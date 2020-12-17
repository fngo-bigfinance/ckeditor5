How to Ckeditor5 Build
=======================
현재 사용하고 있는 에디터의 위치는<br>
package/ckeditor5-build-classic 을 사용하고 있습니다.
1. 플러그인 추가 방법
1. 빌드방법
3. 커밋 방법
4. 프로젝트에서 사용하는 방법



우선 각 빌드될 폴더마다 pakcage.json 이 따로 존재합니다. 추가적인 라이브러리를 설치하여 사용하려면
<br> packages/ckeditor5-build-classic/src
<br> 폴더에 들어가서 해당 라이브러리를 설치하면 됩니다.
<br>
- example
<br> cd packages/ckeditor5-build-classic/src
<br> npm -i font-color

<br> ckeditor.js 파일에 설치한 모듈을 임포트 해줍니다
<br>import SimpleUploadAdapter from '@ckeditor/ckeditor5-upload/src/adapters/simpleuploadadapter';

builtinPlugin 배열에
<br><br>ClassicEditor.builtinPlugins = [
  <br>  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;....
  <br>  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;SImpleUploadAdapter
  <br> ]

  로 설치한 라이브러리를 추가해 준다음에 빌드를 합니다.
<br>
이후 경로를 잘 확인한 후에 yarn run build 을 하게되면 <Br>
ckeditor5-build-classic/build 폴더에 컴파일 된 파일이 나오게 됩니다.

<br><br>
src 는 react에서 사용하진 않지만 변경사항을 알기 위하여 build 폴더와 같이 머지 하시면 됩니다.
<br>

admin-front 에서 사용방법은 package.json 에 해당 의존성을 추가해 주면 됩니다.
<br>{
<br>  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"name": "front",
<br>  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"version": "0.1.0",
<br>  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"private": true,
<br>  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"dependencies": {
<br>  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  ...,
<br>  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  "fngo-ckeditor": "fngo-bigfinance/ckeditor5#feature/simpleupload", github / repository / branch 순서입니다
