---
layout: default
---

{% assign id = page.url | split: 'id=' | last %}
{% assign product = site.data.products | where: "id", id | first %}

{% if product %}

  <h2>{{ product.name }}</h2>
  <p>{{ product.description }}</p>
  <p><strong>Giá:</strong> {{ product.price }}₫</p>
  <a href="/catalog">← Quay lại Catalog</a>
{% else %}
  <p>Không tìm thấy sản phẩm</p>
{% endif %}
