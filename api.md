## Методы:

`BASE_URL` = https://www.shinservice.ru/api/auto

#### Получение производителей авто
GET /brands/

Response:
```
ResponseInterface {
     message: string,
     data: BrandItem[]
}

BrandItem {
   key: string,
   value: string
}
```

#### Получение моделей авто по производителю
GET /models/**<brandItem.key>**/

Response:
```
ResponseInterface {
     message: string,
     data: ModelItem[]
}

ModelItem {
   key: string,
   value: string
}
```

#### Получение поколений авто по модели
GET /generations/**<modelItem.key>**/

Response:
```
ResponseInterface {
     message: string,
     data: GenerationItem[]
}

GenerationItem {
   key: string,
   value: string
}
```

#### Получение модификаций авто по поколению
GET /modifications/**<generationItem.key>**/

Response:
```
ResponseInterface {
     message: string,
     data: ModificationItem[]
}

ModificationItem {
   key: string,
   value: string,
   code_1c: string
}
```
