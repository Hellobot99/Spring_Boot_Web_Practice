# Spring Boot Web Practice Project

Spring Boot와 JSP를 활용하여 웹 애플리케이션의 핵심 기능인 **사용자 인증(Authentication)** 및 **인가(Authorization)**, 게시판 기초 구조를 구현한 학습용 프로젝트입니다.
**Spring Security**를 적용하여 안전한 로그인/회원가입 로직을 구축하였으며, **MyBatis(Mapper)** 패턴을 사용하여 데이터베이스와 연동하였습니다.

## 🛠 Tech Stack

### Backend
- **Java**: 17 (Recommended)
- **Framework**: Spring Boot 3.x
- **Security**: Spring Security (Login, BCrypt Password Encoder)
- **Persistence**: MyBatis (UserMapper)
- **Build Tool**: Gradle

### Frontend
- **Template Engine**: JSP (JavaServer Pages)
- **Styling**: Custom CSS (`/resources/css`)
- **Structure**: Header/Footer Layout (`include` pattern)

## 📂 Project Structure

```text
src/main/
├── java/com/ktj4060/personal_project1/
│   ├── config/          # SecurityConfig (보안 설정)
│   ├── controller/      # PageController, UserController (웹 요청 처리)
│   ├── entity/          # User, Role, CustomUser (DB 모델 및 UserDetails 구현)
│   ├── mapper/          # UserMapper (DB 접근 인터페이스)
│   ├── service/         # UserDetailsServiceImpl (비즈니스 로직)
│   └── PersonalProject1Application.java
└── webapp/
    ├── WEB-INF/views/   # JSP Views
    │   ├── common/      # Header, Footer 공통 레이아웃
    │   ├── login/       # 로그인 페이지
    │   ├── register/    # 회원가입 페이지
    │   └── index.jsp    # 메인 페이지
    └── resources/       # CSS, JS, Images
