# Localidades

Montei através de algumas pesquisas a listagem de algumas localidades, dispostas de formas diferentes, para diferentes formas de uso.\
Abaixo descrevo a estrutura base para cada arquivo/formato:

## JSON

---

### Lista de Países em formato JSON

[./countries.json](./countries.json) - 
Esta é uma listagem de países na seguinte estrutura:

```json
[
  
  {
    "inter" : "Afghanistan", // Nome do País no padrão internacional
    "ptbr" : "Afeganistão",  // Nome do País em português
    "cod" : "AF"             // Sigla exclusiva em 2 chars
  },
  ...
]
```

---

### Lista dos Estados Brasileiros em formato JSON

[./brazil-states.json](./brazil-states.json) - 
Esta é uma listagem dos estados brasileiros na seguinte estrutura:

```json
[
  {
    "cod":"ac",   // Sigla exclusiva em 2 chars
    "nome":"Acre" // Nome do Estado Brasileiro
  },
  ...
]
```

---

### Lista das Cidades com Estados Brasileiros em formato JSON

[./brazil-localities_array.json](./brazil-localities_array.json) - 
Esta é uma listagem de todas as Cidades Brasileiras, segmentada por Estado com Array, na seguinte estrutura:
```json
[ // Lista dos estados
  {
    "cod":"ac",      // Sigla do estado em 2 chars
    "nome":"Acre",   // Nome do Estado Brasileiro
    "cidades": [     // Lista das cidades deste Estado
      {
        "cod":"acrelandia", // Nome da Cidade em minúsculo e sem acento (com espaço)
        "nome":"Acrelândia" // Nome da Cidade Brasileira
      },
      ...
    ]
  },
  ...
]
```

[./brazil-localities_object.json](./brazil-localities_object.json) - 
Esta é uma listagem de todas as Cidades Brasileiras, segmentada por Estado como objeto, na seguinte estrutura:
```json
{ // estados no primeiro nível do objeto
  "ac": {       // Objeto nomeado com sua sigla em 2 chars
    "cod":"ac",      // Sigla do estado em 2 chars
    "nome":"Acre",   // Nome do Estado Brasileiro
    "cidades": [     // Lista das cidades deste Estado
      {
        "cod":"acrelandia", // Nome da Cidade em minúsculo e sem acento (com espaço)
        "nome":"Acrelândia" // Nome da Cidade Brasileira
      },
      ...
    ]
  },
  ...
}
```
> Se você já tem o estado, e quer recuperar apenas suas cidades, na arquitetura de objeto, você economiza processamento.\
> ```Ex.: List['sp'].cidades // desta forma você já terá todas as cidades de São Paulo```


[./brazil-localities_list.json](./brazil-localities_list.json) - 
Esta é uma listagem de todas as Cidades Brasileiras, sem segmentação, na seguinte estrutura:
```json
[ // Lista das Cidades Brasileiras
  {
    "estado_cod":"ac",          // Sigla do estado em 2 chars
    "estado":"Acre",            // Nome do Estado Brasileiro
    "cidade_cod":"acrelandia",  // Nome da Cidade em minúsculo e sem acento (com espaço)
    "cidade":"Acrelândia"       // Nome da Cidade Brasileira
  },
  ...
]
```

### Lista das Cidades separado por Estados Brasileiros em formato JSON

- [AC - ./brazil/ac.json](./brazil/ac.json)
- [AL - ./brazil/al.json](./brazil/al.json)
- [AM - ./brazil/am.json](./brazil/am.json)
- [AP - ./brazil/ap.json](./brazil/ap.json)
- [BA - ./brazil/ba.json](./brazil/ba.json)
- [CE - ./brazil/ce.json](./brazil/ce.json)
- [DF - ./brazil/df.json](./brazil/df.json)
- [ES - ./brazil/es.json](./brazil/es.json)
- [GO - ./brazil/go.json](./brazil/go.json)
- [MA - ./brazil/ma.json](./brazil/ma.json)
- [MG - ./brazil/mg.json](./brazil/mg.json)
- [MS - ./brazil/ms.json](./brazil/ms.json)
- [MT - ./brazil/mt.json](./brazil/mt.json)
- [PA - ./brazil/pa.json](./brazil/pa.json)
- [PB - ./brazil/pb.json](./brazil/pb.json)
- [PE - ./brazil/pe.json](./brazil/pe.json)
- [PI - ./brazil/pi.json](./brazil/pi.json)
- [PR - ./brazil/pr.json](./brazil/pr.json)
- [RJ - ./brazil/rj.json](./brazil/rj.json)
- [RN - ./brazil/rn.json](./brazil/rn.json)
- [RO - ./brazil/ro.json](./brazil/ro.json)
- [RR - ./brazil/rr.json](./brazil/rr.json)
- [RS - ./brazil/rs.json](./brazil/rs.json)
- [SC - ./brazil/sc.json](./brazil/sc.json)
- [SE - ./brazil/se.json](./brazil/se.json)
- [SP - ./brazil/sp.json](./brazil/sp.json)
- [TO - ./brazil/to.json](./brazil/to.json)

Estas são listagens de todas as Cidades Brasileiras por Estado, separado por arquivos, na seguinte estrutura:
```json
[ // Lista das Cidades do Estado
  {
    "value":"Acrelândia", // Nome da Cidade Brasileira
    "key":"acrelandia"    // Nome da Cidade em minúsculo e sem acento (com espaço)
  },
  ...
]
```



---
⌨️ com ❤️ por [André Borali](https://github.com/andreborali) 😊