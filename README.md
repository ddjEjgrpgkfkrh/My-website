<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>기능성식품 안내</title>
<style>
  body { font-family: Arial, sans-serif; margin: 20px; background: #f9f9f9; }
  h1 { color: #2c3e50; }
  table { border-collapse: collapse; width: 100%; background: #fff; }
  th, td { border: 1px solid #ddd; padding: 10px; text-align: left; }
  th { background-color: #3498db; color: white; }
  tr:hover { background-color: #f1f1f1; }
  img { width: 80px; height: auto; border-radius: 8px; }
</style>
</head>
<body>

<h1>기능성식품 안내</h1>

<table>
  <thead>
    <tr>
      <th>이미지</th>
      <th>제품명</th>
      <th>기능성 내용</th>
      <th>제조사</th>
      <th>유통기한</th>
    </tr>
  </thead>
  <tbody id="productTableBody">
    <!-- JS가 여기에 데이터 삽입 -->
  </tbody>
</table>

<script>
// 예시 데이터 (이미지 URL 포함)
const products = [
  {
    name: "홍삼정 에브리타임",
    function: "면역력 증진, 피로 개선",
    manufacturer: "정관장",
    expiration: "2025-12-31",
    image: "https://image.kyobobook.co.kr/newimages/giftshop_new/goods/400/2318/hotdeal_5802318.jpg"
  },
  {
    name: "프로바이오틱스 골드",
    function: "장 건강 개선",
    manufacturer: "락토핏",
    expiration: "2024-08-15",
    image: "https://cdn-pro-web-232-117.cdn-nhncommerce.com/lacto666_godomall_com/data/goods/22/03/13/1000000668/1000000668_detail_011.png"
  },
  {
    name: "오메가3 플러스",
    function: "혈행 개선, 기억력 개선",
    manufacturer: "뉴트리코어",
    expiration: "2025-03-01",
    image: "https://www.nutricore.co.kr/shop/data/goods/1624253017167l0.jpg"
  }
];

const tbody = document.getElementById('productTableBody');
products.forEach(product => {
  const row = document.createElement('tr');
  row.innerHTML = `
    <td><img src="${product.image}" alt="${product.name}"></td>
    <td>${product.name}</td>
    <td>${product.function}</td>
    <td>${product.manufacturer}</td>
    <td>${product.expiration}</td>
  `;
  tbody.appendChild(row);
});
</script>

</body>
</html>
