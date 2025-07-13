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
</style>
</head>
<body>

<h1>기능성식품 안내</h1>

<table>
  <thead>
    <tr>
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
// 예시 데이터 (실제로는 크롤링 혹은 API로 받아와야 함)
const products = [
  {
    name: "홍삼정 에브리타임",
    function: "면역력 증진, 피로 개선",
    manufacturer: "정관장",
    expiration: "2025-12-31"
  },
  {
    name: "프로바이오틱스 골드",
    function: "장 건강 개선",
    manufacturer: "락토핏",
    expiration: "2024-08-15"
  },
  {
    name: "오메가3 플러스",
    function: "혈행 개선, 기억력 개선",
    manufacturer: "뉴트리코어",
    expiration: "2025-03-01"
  }
];

const tbody = document.getElementById('productTableBody');
products.forEach(product => {
  const row = document.createElement('tr');
  row.innerHTML = `
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
