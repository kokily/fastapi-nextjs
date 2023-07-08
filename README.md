<p align="center">
  <img src="https://assets.vercel.com/image/upload/v1588805858/repositories/vercel/logo.png" height="96">
  <h3 align="center">Next.js FastAPI</h3>
</p>

<p align="center">Simple Next.js boilerplate that uses <a href="https://fastapi.tiangolo.com/">FastAPI</a> as the API backend.</p>

## How It Works
Python/FastAPI 서버는 `/api/` 아래의 Next.js 앱에 매핑됩니다.  
`/api/:path*`에 대한 모든 요청을 `/api` 폴더에서 호스팅되는 FastAPI API에 매핑하기 위해 [`next.config.js` rewrites](https://github.com/digitros/nextjs-fastapi/blob/main/next.config.js)를 사용하여 구현됩니다.  
localhost에서는 FastAPI 서버가 실행 중인 '127.0.0.1:8000' 포트에 재작성이 이루어집니다.  
프로덕션에서 FastAPI 서버는 Vercel에서 [Python serverless functions](https://vercel.com/docs/concepts/functions/serverless-functions/runtimes/python)로 호스팅됩니다.


## Getting Started

먼저 Dependencies를 설치합니다:

```bash
npm install
# or
yarn
# or
pnpm install
```

그런 다음 개발 서버를 실행하세요:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
```

결과를 보려면 브라우저에서 [http://localhost:3000](http://localhost:3000)를 여세요.

FastApi 서버는 [http://127.0.0.1:8000](http://127.0.0.1:8000)에서 실행됩니다.  
`package.json`에서 포트를 자유롭게 변경할 수 있습니다(`next.config.js`에서도 업데이트해야 함).