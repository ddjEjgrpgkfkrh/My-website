<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>맞춤형 기능성 식품 추천</title>
<style>
  body { font-family: Arial, sans-serif; max-width: 700px; margin: auto; padding: 20px; }
  select, button { margin-top: 10px; padding: 8px; }
  .product { margin-top: 20px; border-top: 1px solid #ccc; padding-top: 10px; }
  img { max-width: 150px; display: block; margin-top: 5px; }
</style>
</head>
<body>
<h1>맞춤형 기능성 식품 추천</h1>
<p>건강 목표를 선택하면 관련 제품을 추천해 드립니다.</p>

<select id="goal">
  <option value="">-- 건강 목표 선택 --</option>
  <option value="immunity">면역력 강화</option>
  <option value="heart">혈행 개선</option>
</select>
<button onclick="showProducts()">추천 받기</button>

<div id="result"></div>

<script>
// 제품 데이터 (JavaScript 변수에 하드코딩)
const products = [
  {name: "홍삼정 에브리타임", function: "면역력 증진, 피로 개선", goal: "immunity", image: "https://via.placeholder.com/150?text=홍삼"},
  {name: "프로바이오틱스 유산균", function: "장 건강, 면역력 강화", goal: "immunity", image: "https://via.placeholder.com/150?text=유산균"},
  {name: "오메가-3 캡슐", function: "혈중 중성지질 개선, 혈행 개선", goal: "heart", image: "https://via.placeholder.com/150?text=오메가3"}
];

function showProducts() {
  const goal = document.getElementById("goal").value;
  const resultDiv = document.getElementById("result");
  if (!goal) {
    resultDiv.innerHTML = "<p>건강 목표를 선택해주세요.</p>";
    return;
  }
  const filtered = products.filter(p => p.goal === goal);
  if (filtered.length === 0) {
    resultDiv.innerHTML = "<p>해당 목표에 맞는 제품이 없습니다.</p>";
    return;
  }
  let html = "";
  filtered.forEach(p => {
    html += `
      <div class="product">
        <strong>${p.name}</strong><br/>
        기능성: ${p.function}<br/>
        <img src="${p.image}" alt="${p.name} 이미지">
      </div>
    `;
  });
  resultDiv.innerHTML = html;
}
</script>
</body>
</html>
