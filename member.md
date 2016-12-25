# Profile

## Mendapatkan data publik Profile berdasarkan ID

TODO: Sebaiknya mirip dengan struktur hasil [ORCID API](https://members.orcid.org/api). Contoh:

Request:

```
GET /api/profiles/1
Authorization: Bearer {{token}}
Accept: application/json
```

Response:

```json
{
  "name": "Yusuf Habibur Rahman"
}
```

## Mencari Profile berdasarkan Nama

```
GET /api/profiles/search/findAllByNameTerm?q=yusuf
Accept: application/json
Authorization: Bearer {{token}}
```

Hasilnya adalah

```json
{
  "_embedded": {
    "profiles": [
      {
        "name": "Yusuf Habibur Rahman"
      }
    ]
  },
  "page": {
    "size": 10,
    "totalElements": 91,
    "totalPages": 10,
    "number": 0
  }}
```

## Mencari Profiles berdasarkan Pekerjaan \(_job title_ atau _organization_\)

```
GET /api/profiles/search/findAllWorkTerm?q=scripthink
Accept: application/json
Authorization: Bearer {{token}}
```

Hasilnya adalah

```json
{
  "_embedded": {
    "profiles": [
      {
        "name": "Yusuf Habibur Rahman"
      }
    ]
  },
  "page": {
    "size": 10,
    "totalElements": 91,
    "totalPages": 10,
    "number": 0
  }}
```

## TODO: ORCID Compatibility

TODO: Sebaiknya mirip atau mengakomodasi struktur hasil [ORCID API](https://members.orcid.org/api). Contoh:

Request:

```
GET https://orcid.org/0000-0002-5231-2802
Accept: application/json
```

Response:

```json
{
  "message-version": "1.1",
  "orcid-profile": {
    "orcid": null,
    "orcid-id": null,
    "orcid-identifier": {
      "value": null,
      "uri": "http://orcid.org/0000-0002-5231-2802",
      "path": "0000-0002-5231-2802",
      "host": "orcid.org"
    },
    "orcid-deprecated": null,
    "orcid-preferences": {
      "locale": "EN"
    },
    "orcid-history": {
      "creation-method": "WEBSITE",
      "completion-date": null,
      "submission-date": {
        "value": 1466440948207
      },
      "last-modified-date": {
        "value": 1480495344120
      },
      "claimed": {
        "value": true
      },
      "source": null,
      "deactivation-date": null,
      "verified-email": null,
      "verified-primary-email": null,
      "visibility": null
    },
    "orcid-bio": {
      "personal-details": {
        "given-names": {
          "value": "Hendy",
          "visibility": null
        },
        "family-name": {
          "value": "Irawan",
          "visibility": null
        },
        "credit-name": null,
        "other-names": null
      },
      "biography": {
        "value": "Master of Science in Electrical Engineering from Institut Teknologi Bandung, Indonesia.\n\nMy research interest is Semantic Knowledge Base for Lumen AI and Robot Friend. My goal is to develop a practical natural language interaction capabilities with semantic reasoning capabilities to augment intelligent software, devices, and robots.",
        "visibility": "PUBLIC"
      },
      "researcher-urls": {
        "researcher-url": [
          {
            "url-name": {
              "value": "Lumen AI Research Group"
            },
            "url": {
              "value": "http://lumen.lskk.org/"
            }
          },
          {
            "url-name": {
              "value": "figshare"
            },
            "url": {
              "value": "https://figshare.com/authors/Hendy_Irawan/2919542"
            }
          },
          {
            "url-name": {
              "value": "GitHub @ceefour"
            },
            "url": {
              "value": "https://github.com/ceefour"
            }
          },
          {
            "url-name": {
              "value": "Twitter @hendyirawan"
            },
            "url": {
              "value": "https://twitter.com/hendyirawan"
            }
          },
          {
            "url-name": {
              "value": "HendyIrawan.com"
            },
            "url": {
              "value": "https://www.hendyirawan.com/"
            }
          },
          {
            "url-name": {
              "value": "LinkedIn"
            },
            "url": {
              "value": "https://www.linkedin.com/in/hendyirawan"
            }
          }
        ],
        "visibility": "PUBLIC"
      },
      "contact-details": {
        "email": [],
        "address": {
          "country": {
            "value": "ID",
            "visibility": "PUBLIC"
          }
        }
      },
      "keywords": {
        "keyword": [
          {
            "value": "Drools"
          },
          {
            "value": "Institut Teknologi Bandung"
          },
          {
            "value": "Linked Data"
          },
          {
            "value": "artificial intelligence"
          },
          {
            "value": "business process management"
          },
          {
            "value": "jBPM"
          },
          {
            "value": "robotics"
          },
          {
            "value": "rule engine"
          },
          {
            "value": "semantic"
          },
          {
            "value": "workflow engine"
          }
        ],
        "visibility": "PUBLIC"
      },
      "external-identifiers": {
        "external-identifier": [
          {
            "orcid": null,
            "external-id-orcid": null,
            "external-id-common-name": {
              "value": "Loop profile"
            },
            "external-id-reference": {
              "value": "386607"
            },
            "external-id-url": {
              "value": "http://loop.frontiersin.org/people/386607/overview?referrer=orcid_profile"
            },
            "external-id-source": null,
            "source": null
          }
        ],
        "visibility": "PUBLIC"
      },
      "delegation": null,
      "scope": null
    },
    "orcid-activities": {
      "affiliations": null,
      "orcid-works": null,
      "funding-list": null
    },
    "orcid-internal": null,
    "type": "USER",
    "group-type": null,
    "client-type": null
  },
  "orcid-search-results": null,
  "error-desc": null
}
```





