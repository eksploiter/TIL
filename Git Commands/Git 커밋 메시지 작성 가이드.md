<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
</head>
<body>

  <h1>Git 커밋 메시지 작성 가이드</h1>

  <p>이 문서는 프로젝트 관리 및 협업을 위한 Git 커밋 메시지 작성 가이드입니다. 명확하고 일관된 커밋 메시지를 통해 프로젝트의 변경 이력을 보다 쉽게 관리할 수 있습니다.</p>

  <h2>1. 커밋 메시지 작성 규칙</h2>
  <ul>
    <li>제목은 명령문으로, 50자 이내</li>
    <li>본문이 있을 경우, 한 줄 띄우고 작성</li>
    <li>문장의 끝에 마침표 <strong>생략</strong></li>
    <li>한글/영문 혼용 가능하나 팀 규칙에 따름</li>
  </ul>

  <h2>2. 커밋 타입 예시 (Conventional Commits)</h2>
  <ul>
    <li><code>feat</code>: 새로운 기능 추가</li>
    <li><code>fix</code>: 버그 수정</li>
    <li><code>docs</code>: 문서 수정</li>
    <li><code>style</code>: 코드 포맷팅, 세미콜론 누락 등 변경</li>
    <li><code>refactor</code>: 코드 리팩토링 (기능 변경 없음)</li>
    <li><code>test</code>: 테스트 코드 추가 또는 수정</li>
    <li><code>chore</code>: 빌드/설정/패키지 작업</li>
  </ul>

  <h2>3. 커밋 메시지 예시</h2>
  <pre><code>feat: 로그인 기능 추가
fix: 비밀번호 검증 오류 수정
chore: remove node_modules from git tracking
docs: Git 커밋 메시지 가이드 추가</code></pre>

  <h2>4. 실전 커밋 예시 </h2>
  <ul>
    <li><code>feat: Apply .gitignore to remove tracked files like node_modules</code></li>
    <li><code>docs: Add IntelliJ shortcut list in HTML format</code></li>
    <li><code>docs: Git commit message guide 작성</code></li>
  </ul>

  <h2>5. Git 명령어 설명</h2>

  <pre><code>git rm -r --cached node_modules</code></pre>
  <p><strong>설명:</strong> 이미 Git에 올라간 <code>node_modules</code> 폴더를 <strong>Git의 추적 대상에서만 제거</strong>합니다. 로컬 폴더는 삭제되지 않습니다.</p>

  <pre><code>git commit -m "chore: remove node_modules from git tracking"</code></pre>
  <p><strong>설명:</strong> 추적 해제를 <strong>커밋</strong>합니다. <code>chore</code> 타입은 코드 변경 없이 설정, 패키지 관련 작업에 사용됩니다.</p>

  <pre><code>git push origin main</code></pre>
  <p><strong>설명:</strong> 변경 사항을 <strong>원격 저장소(GitHub)의 main 브랜치</strong>에 반영합니다.</p>

  <h2>6. 결과 확인</h2>
  <p>이 과정을 거치면 <code>node_modules</code>는 더 이상 Git에 포함되지 않고, <code>.gitignore</code> 규칙에 따라 추적되지 않습니다.</p>

</body>
</html>
