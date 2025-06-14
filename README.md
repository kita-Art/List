# 📜 한국어 명언 랜덤 생성기 (Korean Quote Generator)

이 프로젝트는 웹 브라우저에서 사용할 수 있는 간단한 한국어 명언 랜덤 생성기입니다. 외부 API를 통해 명언을 가져오고, '다음' 버튼을 눌러 새로운 명언을 볼 수 있으며, 마음에 드는 명언은 즐겨찾기 목록에 추가하여 보관할 수 있습니다.

![bandicam 2025-05-28 13-48-24-041 (1)](https://github.com/user-attachments/assets/bbedcad0-645f-4aae-b427-7e8b83822de5)

## 🚀 주요 기능

* **명언 랜덤 생성:** '다음' 버튼을 클릭할 때마다 한국어 명언 Open API를 통해 새로운 명언을 가져와 표시합니다.
* **로딩 스피너:** 명언을 가져오는 동안 로딩 애니메이션을 표시하여 사용자 경험을 향상시킵니다.
* **즐겨찾기 명언 저장:** 현재 표시된 명언을 '선택' 버튼을 클릭하여 즐겨찾기 목록에 추가할 수 있습니다.
* **중복 저장 방지:** 이미 즐겨찾기 목록에 있는 명언은 다시 저장되지 않도록 방지합니다.

## 🛠️ 기술 스택

이 프로젝트는 웹 개발의 가장 기본적인 요소들로 구성되어 있습니다.

* **HTML5:** 웹 페이지의 구조와 콘텐츠를 구성합니다.
* **CSS3:** 웹 페이지의 시각적인 스타일링(레이아웃, 색상, 폰트 등)을 담당합니다.
    * Google Fonts (`Roboto`)를 사용하여 가독성 좋은 폰트를 적용했습니다.
* **JavaScript (ES6+):** 웹 페이지의 동적인 기능(API 호출, DOM 조작, 이벤트 처리 등)을 구현합니다.
    * `async/await`를 사용하여 비동기 API 호출을 처리했습니다.
    * `localStorage`를 활용하여 현재 명언을 임시 저장합니다.
* **한국어 명언 Open API:** [https://korean-advice-open-api.vercel.app/api/advice](https://korean-advice-open-api.vercel.app/api/advice) 를 사용하여 명언 데이터를 가져옵니다.

## ⚙️ 설치 및 실행 방법

1.  **레포지토리 클론:**
    ```bash
    git clone [https://github.com/Kita-Art/korean-quote-generator.git](https://github.com/Kita-Art/korean-quote-generator.git)
    ```
2.  **프로젝트 폴더로 이동:**
    ```bash
    cd korean-quote-generator
    ```
3.  **파일 열기:**
    `index.html` 파일을 웹 브라우저로 직접 엽니다. (예: 크롬 브라우저에서 `index.html` 파일을 더블 클릭)

## ✨ 배운 점 및 개선 사항

이 프로젝트를 통해 다음과 같은 것들을 배우고 경험했습니다.

* **HTML/CSS 기본기:** 웹 페이지의 구조를 설계하고, `display: flex`를 활용하여 요소를 중앙에 배치하는 등 기본적인 레이아웃 및 스타일링 방법을 익혔습니다.
* **JavaScript DOM 조작:** JavaScript를 사용하여 HTML 요소를 선택하고(`querySelector`, `getElementById`), 텍스트를 변경하거나(`innerText`), 스타일을 제어하고(`style.display`), 동적으로 요소를 추가(`appendChild`)하는 방법을 실습했습니다.
* **비동기 API 통신:** `fetch` API와 `async/await` 문법을 사용하여 외부 API를 호출하고 데이터를 가져오는 비동기 통신 과정을 이해하고 구현했습니다. 네트워크 요청 시 발생할 수 있는 에러 처리(`try-catch`)의 중요성을 깨달았습니다.
* **이벤트 리스너 활용:** 버튼 클릭 이벤트를 감지하고(`addEventListener`), 해당 이벤트에 따라 특정 함수가 실행되도록 구현했습니다.
* **로컬 스토리지 활용 (개선점):** 현재 명언을 `localStorage`에 저장하는 기능을 추가했지만, 이는 페이지 새로고침 시 즐겨찾기 목록이 초기화된다는 한계를 가지고 있습니다. **향후 개선점으로는 즐겨찾기 목록 자체를 `localStorage`에 배열 형태로 저장하여 페이지를 다시 로드해도 유지되도록 구현해 볼 예정입니다.**
* **사용자 피드백 개선 (개선점):** 명언이 이미 저장되었을 때 `alert()` 대신 더 부드러운 UI 메시지를 제공하는 방법을 고려해 볼 수 있습니다.
* **코드 모듈화 (개선점):** 현재 `script.js` 파일에 모든 로직이 들어있는데, 함수별로 역할을 분리하거나, `Class`를 사용하여 코드의 재사용성과 유지보수성을 높이는 방법을 고민해 볼 것입니다.
