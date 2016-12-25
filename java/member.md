# Profile

```typescript
import {ProfileService} from './profile/profile.service';
```

## Mencari profile berdasarkan keyword nama

```typescript
profileService.findAllByNameTerm('yusuf')
  .subscribe(data => {
    this.profiles = data._embedded.profiles;
  }, error => {
    window.alert(error.exception + ': ' + error.message);
  });
```

Referensi: Lihat [](/member.md)

## Mencari profile berdasarkan keyword pekerjaan \(_job title_ atau _organization_\)

```typescript
profileService.findAllByWorkTerm('programmer')
  .subscribe(data => {
    this.profiles = data._embedded.profiles;
  }, error => {
    window.alert(error.exception + ': ' + error.message);
  });
```

Referensi: Lihat [](/member.md)
