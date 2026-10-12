# 알파카 타이머 개인정보처리방침

시행일: 2026년 10월 12일 (아이폰판 내용 추가)

알파카 타이머(이하 "앱")는 알파카체리스튜디오(이하 "개발자")가 만든 집중용 앱 잠금 앱입니다.
이 방침은 앱이 어떤 정보를 다루고, 어떻게 보호하는지 설명합니다.

## 1. 한 줄 요약

**개발자는 개인정보를 수집하지 않으며, 앱이 기록한 내용(약속 시간, 고른 앱, 집중 기록 등)은 기기 밖으로 보내지 않습니다.**
앱에는 회원가입, 로그인, 서버가 없습니다.
다만 안드로이드판은 무료로 제공하기 위해 **구글 애드몹(AdMob) 광고**를 보여 주며, 광고 제공 과정에서 구글이 광고 식별자 등을 처리할 수 있습니다 (6번 참고). 아이폰판에는 광고가 없습니다.

## 2. 기기 안에만 저장되는 정보

앱이 동작하려면 아래 정보를 **사용자의 기기 안에만** 저장합니다. 개발자는 이 정보를 볼 수 없습니다.

| 정보 | 쓰는 곳 |
| --- | --- |
| 약속(잠금) 시작·끝 시각 | 정한 시간 동안 앱을 잠그고, 시간이 되면 저절로 풀기 위해 |
| 공부에 꼭 필요한 앱(열어 둘 앱)으로 고른 앱, 열공모드 켜짐 여부 | 어떤 앱을 막을지 정하기 위해 |
| 숨구멍 남은 횟수, 참은 횟수, 푼 문제 수 | 잠금 화면과 완료 화면에 보여 주기 위해 |
| 알파카 레벨·경험치, 날짜별 집중 기록 | 성장·기록 화면에 보여 주기 위해 |

이 정보는 앱을 삭제하면 함께 지워집니다.

## 3. 설치된 앱 목록 (안드로이드)

열어 둘 앱을 고를 수 있도록, 기기 홈 화면에 보이는 앱의 **이름과 아이콘**을 불러와 화면에 보여 줍니다.
이 목록은 기기 안에서만 쓰이며 저장하거나 밖으로 보내지 않습니다.

## 4. 접근성 서비스(AccessibilityService) 사용 안내

앱의 핵심 기능인 "약속한 시간 동안 고른 앱 막기"를 위해 안드로이드 **접근성 서비스**를 사용합니다.
사용자가 안드로이드 설정에서 직접 켜야 동작합니다.

- **확인하는 것:** 지금 화면 맨 앞에 뜬 앱이 **어떤 앱인지(패키지 이름)** 만 확인합니다.
- **확인하지 않는 것:** 화면 내용, 입력한 글자, 비밀번호, 메시지, 알림 내용 등은 **읽지 않습니다.**
  (설정에서 화면 내용 읽기 권한 자체를 요청하지 않습니다.)
- **하는 일:** 사용자가 잠그기로 한 앱이 약속 시간 중에 열리면, 그 앱 대신 알파카 타이머 화면을 띄웁니다.
  약속 시간이 끝나면 아무것도 막지 않습니다.
- **보내지 않음:** 확인한 정보는 저장하거나 기기 밖으로 보내지 않습니다.

접근성 서비스는 언제든지 안드로이드 설정 → 접근성 → 설치된 앱 → 알파카 타이머에서 끌 수 있습니다.

## 4-1. 스크린타임 API (아이폰)

아이폰판은 접근성 서비스 대신 애플의 **스크린타임 API(Family Controls · Managed Settings · Device Activity)** 로 앱을 막습니다.
처음 한 번 사용자가 스크린타임 권한을 허용해야 동작합니다.

- **열어 둘 앱 고르기:** 애플이 제공하는 앱 고르기 화면을 씁니다. 고른 결과는 애플이 만든 **암호화된 토큰**으로만 앱에 전달되어,
  개발자도 앱도 **어떤 앱을 골랐는지 이름을 알 수 없습니다.**
- **하는 일:** 약속 시간 동안 고르지 않은 앱 위에 애플의 잠금 화면(방패)을 씌우고, 끝나는 시각이 되면 저절로 풉니다.
- **사용 기록을 읽지 않음:** 앱 사용 시간, 방문한 웹사이트, 화면 내용 등은 읽거나 모으지 않습니다.
- **보내지 않음:** 위 정보는 기기 안(앱과 앱 확장 기능이 함께 쓰는 저장소)에만 저장되며 기기 밖으로 보내지 않습니다.

스크린타임 권한은 언제든지 아이폰 설정 → 스크린타임 → 「스크린타임 접근 권한이 있는 앱」에서 끌 수 있습니다.

## 5. 그 밖의 권한

- **진동(VIBRATE):** 시간 다이얼을 돌릴 때 "톡톡" 하는 진동을 주기 위해 사용합니다.
- **알림 (아이폰):** 잠긴 앱의 잠금 화면에서 「숨구멍 쓰러 가기」를 누르면 알파카 타이머로 돌아오는 알림을 한 번 보냅니다. 기기 안에서 만드는 알림이며 서버를 거치지 않습니다.

## 6. 광고 (Google AdMob, 안드로이드)

아이폰판에는 광고가 없습니다. 안드로이드판은 앱 홈 화면, 잠금 화면, 약속 완료 화면 아래에 구글 애드몹 배너 광고가 나옵니다.

- 광고를 보여 주기 위해 구글은 **광고 식별자(Advertising ID)**, 기기 정보(기종·OS 버전·언어 등), IP 주소,
  광고 조회·클릭 정보를 수집·처리할 수 있습니다.
- 이 정보는 구글이 광고 제공, 광고 성과 측정, 부정 클릭 방지 등에 쓰며, 처리 방식은
  [구글 개인정보처리방침](https://policies.google.com/privacy)과
  [구글이 파트너 앱의 정보를 사용하는 방식](https://policies.google.com/technologies/partner-sites)을 따릅니다.
- 개발자는 광고 식별자나 위 정보를 따로 받아 보거나 저장하지 않습니다.
- **맞춤 광고 끄기:** 안드로이드 설정 → Google → 광고(또는 개인정보 보호 → 광고)에서 광고 ID를 삭제하거나 재설정할 수 있습니다.

## 7. 제3자 제공

- 개발자는 개인정보를 제3자에게 제공하거나 판매하지 않습니다. (광고는 6번과 같이 구글이 직접 처리합니다.)
- 분석 도구는 쓰지 않습니다.

## 8. 아동의 개인정보

개발자는 만 14세 미만 아동의 개인정보를 따로 수집하지 않습니다. 광고는 구글 애드몹의 정책에 따라 제공됩니다.

## 9. 방침의 변경

이 방침이 바뀌면 이 페이지에 새 내용과 시행일을 올립니다.

## 10. 문의

- 개발자: 알파카체리스튜디오 (Alpaca Cherry Studio)
- 이메일: support@alpacacherrystudio.com

---

# Alpaca Timer Privacy Policy (English)

Effective date: October 12, 2026 (iPhone section added)

**The developer does not collect personal information, and what the app records (focus times, chosen apps,
focus history) never leaves your device.** There is no account, no login, and no server.
The Android app shows **Google AdMob** banner ads to stay free; Google may process data such as the advertising ID (see below). The iPhone app has no ads.

- **Stored on your device only:** focus session start/end times, the apps you chose to keep open
  and whether strict mode is on, break counts, quiz counts, alpaca level and focus history.
  The developer cannot see this data. It is deleted when you uninstall the app.
- **Installed apps list (Android):** the app reads the names and icons of apps on your home screen so you can pick
  which ones to lock. This list is used on the device only and is never stored or transmitted.
- **Accessibility Service:** used only to detect **which app** is in the foreground (package name) during a
  focus session you started, and to show the Alpaca Timer screen instead of an app you chose to lock.
  It does **not** read screen content, text you type, passwords, messages or notifications, and nothing is
  stored or transmitted. You can turn it off at any time in Android Settings → Accessibility.
- **Screen Time API (iPhone):** the iPhone app uses Apple's Family Controls, Managed Settings and Device Activity
  frameworks instead of an accessibility service. Apps you pick in Apple's app picker reach the app only as
  opaque tokens, so neither the app nor the developer can tell which apps you chose. The app shields the other
  apps during a session you started and lifts the shields automatically at the end time. It does not read usage
  history, websites or screen content, and nothing leaves the device. You can revoke access in Settings → Screen Time.
- **Notifications (iPhone):** a local notification that brings you back to Alpaca Timer when you tap
  "숨구멍 쓰러 가기" on a shield. It is created on the device; no server is involved.
- **Vibrate:** for haptic ticks when turning the time dial.
- **Ads (Google AdMob, Android only):** banner ads appear at the bottom of the home, lock and completion screens.
  To serve ads, Google may collect and process the advertising ID, device information (model, OS version,
  language), IP address and ad interaction data, under the
  [Google Privacy Policy](https://policies.google.com/privacy) and
  [How Google uses information from partner apps](https://policies.google.com/technologies/partner-sites).
  The developer does not receive or store this data. You can reset or delete your advertising ID in
  Android Settings → Google → Ads.
- **No other third parties:** the developer does not share or sell data. No analytics are used.
- **Contact:** Alpaca Cherry Studio — support@alpacacherrystudio.com
