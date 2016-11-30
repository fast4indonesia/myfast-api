# Java Client SDK

Java Client SDK digunakan untuk mengakses layanan di MyFAST API menggunakan Android app.

## Member

### Mencari member berdasarkan keyword nama

```java
Pageable<Member> page = memberRepository.findAllByNameTerm("yusuf");
```
