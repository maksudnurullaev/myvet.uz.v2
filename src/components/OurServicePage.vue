<template>
  <!-- view-Home-->
  <div class="container">
    <h1 class="text-center mt-3">Услуги и цены</h1>
    <div class="sticky-top">
      <div class="dropdown">
        <button
          class="btn btn-success dropdown-toggle"
          type="button"
          data-bs-toggle="dropdown"
          aria-expanded="false"
        >
          Быстрый переход
        </button>
        <ul class="dropdown-menu">
          <li
            v-for="(qLink, index) in getQLinksGroup()"
            v-bind:key="'quick-link-' + index"
          >
            <a class="dropdown-item" v-bind:href="qLink.link">{{
              qLink.value
            }}</a>
          </li>
        </ul>
      </div>
    </div>
    <div class="mt-3">
      <table class="table">
        <thead>
          <tr>
            <th scope="col">Название</th>
            <th scope="col">Цена (в сумах)</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="(prow, index) in prices" v-bind:key="'price-row' + index">
            <template v-if="prow.type == 'header'">
              <th
                scope="row"
                colspan="2"
                class="text-center"
                v-bind:id="'group-of-prices-' + index"
              >
                {{ getNumbering(prow) }} {{ prow.value }}
              </th>
            </template>
            <template v-else-if="prow.type == 'row'">
              <td>{{ getNumbering(prow) }} {{ prow.value }}</td>
              <td>{{ formatPriceNumber(prow.price!) }}</td>
            </template>
            <template v-else-if="prow.type == 'group'">
              <td colspan="2" class="text-center">
                {{ getNumbering(prow) }} {{ prow.value }}
              </td>
            </template>
            <template v-else-if="prow.type == 'group-price'">
              <td class="text-end">
                {{ getNumbering(prow) }} {{ prow.value }}
              </td>
              <td>{{ formatPriceNumber(prow.price!) }}</td>
            </template>
            <template v-else-if="prow.type == 'group-price-from'">
              <td class="text-end">
                {{ getNumbering(prow) }} {{ prow.value }}
              </td>
              <td>от {{ formatPriceNumber(prow.price!) }}</td>
            </template>
            <template v-else-if="prow.type == 'row-price-from'">
              <td>{{ getNumbering(prow) }} {{ prow.value }}</td>
              <td>от {{ formatPriceNumber(prow.price!) }}</td>
            </template>
          </tr>
        </tbody>
      </table>
    </div>
    <!-- <pre>
      {{ prices }}
    </pre> -->
  </div>
</template>

<script setup lang="ts">
import prices from "@/stores/prices.json";

const Numbering = {
  N1: 0,
  N12: 0,
  N123: 0,
};

interface prow {
  type: string;
  value: string;
  price?: number | undefined;
}

interface pQLink {
  value: string;
  link: string;
}

function getNumbering(r: prow): string {
  let result = "";
  console.log("r.type", r.type);
  if (r.type == "header") {
    Numbering.N1 = Numbering.N1 + 1;
    result = Numbering.N1 + ".";
    Numbering.N12 = 0;
    Numbering.N123 = 0;
  } else if (
    r.type == "row" ||
    r.type == "row-price-from" ||
    r.type == "group"
  ) {
    Numbering.N12 = Numbering.N12 + 1;
    result = Numbering.N1 + "." + Numbering.N12;
    if (r.type == "group") {
      Numbering.N123 = 0;
    }
  } else if (r.type == "group-price" || r.type == "group-price-from") {
    Numbering.N123 = Numbering.N123 + 1;
    result = Numbering.N1 + "." + Numbering.N12 + "." + Numbering.N123;
  }
  return result;
}

function getQLinksGroup(): pQLink[] {
  const links: pQLink[] = [];
  prices.forEach((element, index) => {
    if (element.type == "header") {
      links.push({ value: element.value, link: "#group-of-prices-" + index });
    }
  });
  return links;
}

function formatPriceNumber(price: number): string {
  return price.toString().replace(/\B(?<!\.\d*)(?=(\d{3})+(?!\d))/g, ",");
}
</script>
