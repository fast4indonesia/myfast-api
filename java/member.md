# Member

## Mencari member berdasarkan keyword nama

```java
Pageable<Member> page = memberRepository.findAllByNameTerm("yusuf");
```

## Mencari member berdasarkan keyword pekerjaan (_job title_ atau _organization_)

```java
Pageable<Member> page = memberRepository.findAllByWorkTerm("yusuf");
```
