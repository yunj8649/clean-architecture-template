[타입스크립트 프로젝트를 위한 궁극적인 클린 아키텍처 템플릿](https://velog.io/@lky5697/the-ultimate-clean-architecture-template-for-typescript-projects#%EC%9E%90%EC%84%B8%ED%95%9C-%EA%B5%AC%ED%98%84-%EA%B0%80%EC%9D%B4%EB%93%9C)  
참고하여 따라해본 프로젝트 입니다. 
  
  
## `package.json` 스크립트 설명 
`build`: 프로젝트를 빌드하면 이 패키지를 다른 패키지에서 가져올 수 있는 `index.d.ts`가 포함된 빌드 폴더가 생성됩니다.  
`build:watch`: 코드가 변경될 때마다 프로젝트가 재빌드 됩니다.  
`rollup`: 빌드 후 프로젝트 타입을 번들합니다. 올바른 선언 및 내보내기를 포함하는 `index.d.ts`를 생성하려면 이 작업이 필요합니다.  
`test`: 패키지의 모든 단위 테스트를 실행합니다.  
`test:watch`: 모든 관련 변경 사항에 대해 테스트를 다시 시작합니다. (자세한 내용은 [jest](https://jestjs.io/docs/cli#--watch) 문서 참조)  



## `devDependencies` 설명 
`rollup`, `rollup-plugin-dts`, `@rollup/plugin-typescript`: `index.d.ts` 파일을 유즈케이스에 더 유용하도록 수정하는 데 사용되는 모듈 번들러입니다.  
`jest`, `ts-jest`: 테스트 작성 및 단위 테스트용  
`nodemon`: 코드가 변경될 때마다 명령을 실행할 수 있습니다. `build:watch` 스크립트를 참조하세요.  
나머지는 타입스크립트 종속성입니다.  


## `tsconfig.build.json`  
빌드에 테스트가 포함되지 않도록 작성


## 빌드 CLI 
``` bash
npm install && npm run build
```
정상적인 빌드 확인은 아래 파일ㄹ에서 확인할 수 있다.
`build/src/index.ts`, `build/src/index.d.ts`




