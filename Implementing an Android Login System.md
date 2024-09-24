# 안드로이드 로그인 시스템 구현

## 1. 회원 가입 및 인증
- Firebase Authentication이나 자체 서버를 사용하여 사원 번호 및 전화번호를 인증할 수 있습니다. Firebase Authentication은 전화번호 인증 기능을 제공합니다.

## 2. 핀번호 로그인
- SharedPreferences나 EncryptedSharedPreferences를 사용하여 핀번호를 로컬에 안전하게 저장한 후, 이후 로그인 시 이 핀번호를 비교하여 인증할 수 있습니다.

## 3. 관할 지역 및 4가지 모드 선택
- 회원 가입 중 사용자가 선택한 지역 및 모드를 서버에 저장하고, 이를 기준으로 해당 모드에 맞는 메인 화면을 보여줄 수 있습니다.

## 4. 메인 화면 분리
- 4가지 모드에 따라 다른 화면을 구성할 수 있습니다. 예를 들어, 모드에 따른 액티비티나 프래그먼트를 구성하여 사용자가 선택한 모드에 맞는 메인 화면을 보여줍니다.

### 간단한 흐름 예시
- 회원 가입 화면: 사용자 정보 입력 (사원 번호, 전화번호 인증)
- 지역 및 모드 선택: 관할 지역 선택, 4가지 모드 중 하나 선택
- 핀번호 설정: 핀번호 4자리 입력 및 저장
- 메인 화면 전환: 사용자가 선택한 모드에 따라 메인 화면을 다르게 구성

## 간단한 코드 예시
- 회원 가입 예시 (전화번호 인증 부분)
```
// Firebase Authentication for phone number verification
PhoneAuthProvider.getInstance().verifyPhoneNumber(
    phoneNumber,         // Phone number to verify
    60,                  // Timeout duration
    TimeUnit.SECONDS,    // Unit of timeout
    this,                // Activity (for callback binding)
    verificationCallbacks) // OnVerificationStateChangedCallbacks
```

- 핀번호 저장 (SharedPreferences 예시)
```
val sharedPreferences = getSharedPreferences("PinPrefs", MODE_PRIVATE)
val editor = sharedPreferences.edit()
editor.putString("PIN_CODE", userPin) // 핀번호 저장
editor.apply()
```

- 모드에 따른 화면 전환 (모드 선택 후)
```
val selectedMode = intent.getIntExtra("MODE", 1)
when (selectedMode) {
    1 -> startActivity(Intent(this, Mode1Activity::class.java))
    2 -> startActivity(Intent(this, Mode2Activity::class.java))
    3 -> startActivity(Intent(this, Mode3Activity::class.java))
    4 -> startActivity(Intent(this, Mode4Activity::class.java))
}
```

---

이와 같은 방식으로 구현하면 사용자가 모드에 따라 다른 메인 화면으로 전환되는 기능을 구현할 수 있습니다. 필요에 따라 디자인 및 기능을 확장하면 됩니다.
