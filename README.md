# 어디까지

OpenStreetMap 장소 검색으로 출발지와 도착지를 찾고, 자동차 이동 거리와 지도 경로를 보여주는 정적 웹앱입니다.
장소 검색 한 번으로 기본 검색 결과의 경로와 거리를 계산하며, 다른 장소 결과를 선택하면 자동으로 갱신됩니다.

## 실행

`index.html`을 브라우저에서 열거나 정적 웹 호스팅에 배포하면 됩니다. 빌드 단계, 서버 함수, Redis, API 키, 환경변수는 필요하지 않습니다. Vercel에서 이 폴더를 프로젝트로 가져오고 Framework Preset을 **Other**로 두면 정적 사이트로 배포됩니다.

## 사용 API

- 장소 검색: [Nominatim](https://nominatim.org/)
- 자동차 경로 및 거리: [OSRM 공개 데모 서버](https://project-osrm.org/)
- 실제 지도 타일 및 지도 링크: [OpenStreetMap](https://www.openstreetmap.org/) (Leaflet으로 경로를 지도 위에 표시)

Nominatim 사용 정책에 따라 입력 중 자동완성 대신 사용자가 검색 버튼을 누를 때만 장소를 조회하며, 두 검색 요청 사이에 간격을 둡니다. 무료 공개 서비스는 사용량 제한과 가용성 정책이 있으며, 이를 보장할 별도 백엔드는 포함하지 않습니다.
