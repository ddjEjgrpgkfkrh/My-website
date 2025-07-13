<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>기능성식품 안내</title>
<style>
  body { font-family: Arial, sans-serif; margin: 20px; background: #f8f8f8; }
  h1 { color: #8b0000; }
  .tabs button { margin-right: 10px; padding: 10px 15px; font-size: 16px; border: none; background-color: #8b0000; color: white; border-radius: 5px; cursor: pointer; }
  .tabs button:hover { background-color: #a52a2a; }
  .section { display: none; background: #fff; padding: 20px; margin-top: 20px; border-radius: 8px; box-shadow: 0 0 5px rgba(0,0,0,0.1); }
  img { max-width: 250px; border-radius: 8px; }
  ul { margin: 0; padding-left: 20px; }
  table { width: 100%; border-collapse: collapse; margin-top: 10px; }
  th, td { border: 1px solid #ccc; padding: 8px; }
  th { background: #d2691e; color: white; }
</style>
</head>
<body>

<h1>기능성식품 계별 안내</h1>

<div class="tabs">
  <button onclick="showSection('immune')">면역계</button>
  <button onclick="showSection('nervous')">신경계</button>
  <button onclick="showSection('endocrine')">내분비계</button>
</div>

<!-- 면역계 섹션 -->
<div id="immune" class="section">
  <h2>면역계 - 홍삼</h2>
  <img src="1000013663.jpg" alt="홍삼정 에브리타임">

  <h3>제조 기준</h3>
  <ul>
    <li>원재료: 수삼(Panax ginseng C.A. Meyer)을 증기 또는 기타방법으로 쪄서 익혀 말린 홍삼</li>
    <li>제조방법: 분말화 또는 추출·여과·농축·발효</li>
    <li>기능성분 함량: 진세노사이드 Rg1, Rb1, Rg3 합계 2.5 mg/g 이상</li>
    <li>제조 시 유의사항: 4년근 이상 인삼근만 사용</li>
  </ul>

  <h3>규격</h3>
  <ul>
    <li>성상: 고유 색택과 향미, 이미·이취 없음</li>
    <li>진세노사이드 Rg1, Rb1, Rg3 합계:
      <ul>
        <li>원료성 제품: 표시량 이상</li>
        <li>최종제품: 표시량의 80% 이상</li>
      </ul>
    </li>
    <li>세균수: 1 mL당 3,000 이하(농축액)</li>
    <li>대장균군: 음성</li>
  </ul>

  <h3>최종제품 요건</h3>
  <ul>
    <li>기능성: 면역력 증진, 피로개선, 혈소판 응집억제 통한 혈액흐름, 기억력 개선, 항산화, 갱년기 여성 건강 도움</li>
    <li>일일 섭취량:
      <ul>
        <li>면역력·피로: 3~80 mg</li>
        <li>혈액흐름·기억력·항산화: 2.4~80 mg</li>
        <li>갱년기 여성 건강: 25~80 mg</li>
      </ul>
    </li>
    <li>섭취 시 주의사항:
      <ul>
        <li>당뇨치료제, 혈액항응고제 복용 시 주의</li>
        <li>알레르기 체질은 과민반응 가능</li>
        <li>이상사례 발생 시 섭취 중단 후 전문가 상담</li>
      </ul>
    </li>
  </ul>

  <h3>비슷한 제품 목록</h3>
  <table>
    <tr><th>제품명</th><th>기능성</th><th>제조사</th></tr>
    <tr><td>한미면역홍삼골드</td><td>인지기능/기억력, 피로, 갱년기 여성, 혈행, 면역, 항산화</td><td>광동제약주식회사</td></tr>
    <tr><td>홍삼정 365플러스</td><td>동일</td><td>광동제약주식회사</td></tr>
    <!-- 필요시 추가 -->
  </table>

  <h3>출처</h3>
  <p><a href="https://data.mfds.go.kr/hid/opbaa01/prdtSrchLst.do" target="_blank">식품의약품안전처 자료 바로가기</a></p>
</div>

<!-- 신경계 섹션 -->
<div id="nervous" class="section">
  <h2>신경계</h2>
  <p>여기에 신경계 관련 기능성식품 정보를 추가할 수 있어요!</p>
</div>

<!-- 내분비계 섹션 -->
<div id="endocrine" class="section">
  <h2>내분비계</h2>
  <p>여기에 내분비계 관련 기능성식품 정보를 추가할 수 있어요!</p>
</div>

<script>
function showSection(id) {
  // 모든 섹션 숨김
  var sections = document.getElementsByClassName('section');
  for(var i=0; i<sections.length; i++){
    sections[i].style.display = 'none';
  }
  // 클릭한 섹션만 표시
  document.getElementById(id).style.display = 'block';
}
</script>

</body>
</html>
