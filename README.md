# Next.js를 이용한 포트폴리오 사이트 만들기
[Next.js](https://nextjs.org/)   
[`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app)   
run the development server: npm run dev   
Open [http://localhost:3000](http://localhost:3000) with your browser to see the result   
You can start editing the page by modifying `app/page.js`. The page auto-updates as you edit the file   
## Next.js를 사용하는 이유
Next.js는 React 기반의 웹 프레임워크로, 클라이언트 측 및 서버 측 렌더링을 지원하여 웹 애플리케이션의 성능을 최적화하는 데 도움이 되는 다양한 기능을 제공합니다.   
1. 서버 측 렌더링(SSR) 및 정적 사이트 생성 (SSG) 지원:   
Next.js는 페이지를 서버에서 사전에 렌더링하여 초기 로딩 속도를 향상시킵니다. 또한, 정적 사이트 생성을 통해 미리 페이지를 생성하여 성능을 최적화할 수 있습니다.   
2. 개발자 친화적인 파일 시스템 기반 라우팅:   
페이지 및 API 엔드포인트를 만들 때 파일 시스템을 기반으로 한 직관적인 라우팅을 제공하여 개발자가 코드를 구성하고 이해하기 쉽게 합니다.   
3. Hot Module Replacement (HMR)을 통한 빠른 개발 환경:   
코드 변경 시 바로 적용되는 HMR을 지원하여 빠른 개발 사이클을 제공하며, 애플리케이션을 다시 시작할 필요 없이 변경 사항을 확인할 수 있습니다.   
4. 자동 코드 분할 (Automatic Code Splitting):   
페이지 및 컴포넌트 단위로 자동으로 코드를 분할하여 필요한 부분만 로드되도록 하여 초기 페이지 로딩 시간을 최적화합니다.   
5. 풍부한 플러그인 생태계:   
다양한 플러그인을 통해 확장성이 뛰어나며, 데이터 가져오기, 이미지 최적화, CSS 처리 등 다양한 기능을 쉽게 통합할 수 있습니다.   
6. TypeScript 및 Babel 지원:   
TypeScript를 기본적으로 지원하며, Babel을 통한 다양한 JavaScript 문법 변환을 지원하여 개발자가 선호하는 언어와 도구를 사용할 수 있습니다.   
7. 배포 및 호스팅 간편성:   
Now, Vercel, Netlify 등과 같은 플랫폼과의 통합이 쉽고, 정적 사이트 생성을 통해 CDN에 캐싱되어 성능이 향상됩니다.   
8. 웹팩과 바벨의 강력한 기능 활용:   
웹팩 및 바벨과 같은 강력한 빌드 도구를 활용하여 최적화된 번들링 및 코드 변환을 제공합니다.   
이러한 특장점들로 Next.js는 개발자에게 효율적이고 성능 최적화가 잘 된 웹 애플리케이션 개발을 도와주는 강력한 도구입니다.   
## 셋팅
`npx create-next-app@latest`   
Ok to proceed? (y) Y   
√ What is your project named? ... .   
√ Would you like to use TypeScript? ... No / Yes    n   
√ Would you like to use ESLint? ... No / Yes    y   
√ Would you like to use Tailwind CSS? ... No / Yes  n   
√ Would you like to use `src/` directory? ... No / Yes  y   
√ Would you like to use App Router? (recommended) ... No / Yes  y   
√ Would you like to customize the default import alias (@/*)? ... No / Yes  y   
√ What import alias would you like configured? ... @/*   

`npm install sass`
`npm install @studio-freight/lenis`
`npm install gsap`

## CSR(React)과 SSR(Next.js)
CSR(클라이언트 측 렌더링)과 SSR(서버 측 렌더링)은 사용자가 보는 화면을 어느 쪽에서 완성하는지에 대한 차이입니다.   
   
CSR (React):   
사용자의 브라우저(클라이언트)에서 초기 페이지 로딩 시에는 기본적인 HTML, CSS, JavaScript 파일을 받아옵니다.   
브라우저는 받아온 자바스크립트를 실행하며, 동적으로 페이지를 구성합니다.   
데이터가 필요한 경우 API를 호출하여 데이터를 가져와 화면을 업데이트합니다.   
검색 엔진 최적화(SEO)에 취약할 수 있습니다.   
   
   
SSR (Next.js):   
사용자의 요청이 있을 때마다 서버에서 초기 페이지를 완성하여 클라이언트에게 전달합니다.   
서버에서 데이터를 미리 가져와 HTML에 포함시켜 클라이언트에게 제공합니다.   
초기 로딩 시에 완전한 HTML이 전달되므로 초기 로딩 속도가 빠르며 SEO에 유리합니다.   
클라이언트는 받아온 HTML을 그대로 화면에 렌더링하므로 추가적인 데이터 요청이 필요하지 않습니다.   
   
      
선택 기준:   
CSR은 동적인 페이지와 부드러운 사용자 경험에 적합하며, 부분적인 업데이트가 자주 발생할 때 유리합니다.   
SSR은 초기 로딩 속도와 SEO에 강점이 있으며, 데이터가 요청마다 변경되지 않고 일정하게 유지될 때 적합합니다.   
프로젝트의 성격과 요구사항에 따라 적절한 방식을 선택하여 사용합니다.   






