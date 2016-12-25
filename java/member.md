# Member

```typescript
import {MemberService} from './member/member.service';
```

## Mencari member berdasarkan keyword nama

```typescript
memberService.findAllByNameTerm('yusuf')
  .subscribe(data => {
    this.members = data._embedded.members;
  }, error => {
    window.alert(error.exception + ': ' + error.message);
  });
```

Referensi: Lihat [](/member.md)

## Mencari member berdasarkan keyword pekerjaan \(_job title_ atau _organization_\)

```typescript
memberService.findAllByWorkTerm('programmer')
  .subscribe(data => {
    this.members = data._embedded.members;
  }, error => {
    window.alert(error.exception + ': ' + error.message);
  });
```

Referensi: Lihat [](/member.md)
