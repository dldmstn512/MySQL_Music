# 🎵 MySQL Music API Server

음악 정보를 관리하고 JSON으로 제공하는 Spring Boot 기반 RESTful API 서버입니다.  
MySQL과 Spring Data JPA를 이용해 데이터베이스 연동을 구현했습니다.

---

## 📌 프로젝트 개요

- **Framework**: Spring Boot 3.5.3
- **Language**: Kotlin
- **DB**: MySQL 8.0
- **JPA**: Spring Data JPA
- **Build Tool**: Gradle (Kotlin DSL)

---

## 📁 주요 기능

| 기능               | 설명 |
|--------------------|------|
| `/songs`           | 전체 노래 리스트를 JSON으로 반환 |
| (예정) `/playlists`| 재생목록 기능 (추가 예정)        |
| (예정) `/users`    | 사용자 기능 (추가 예정)          |

---

## 🛠 프로젝트 실행 방법

### 1. MySQL 데이터베이스 준비
```sql
CREATE DATABASE MySQL_Music;
USE MySQL_Music;

CREATE TABLE songs (
  id INT AUTO_INCREMENT PRIMARY KEY,
  title VARCHAR(255),
  artist VARCHAR(255),
  genre VARCHAR(255)
);

INSERT INTO songs (title, artist, genre) VALUES
('Dynamite', 'BTS', 'Pop'),
('OMG', 'NewJeans', 'K-pop');
