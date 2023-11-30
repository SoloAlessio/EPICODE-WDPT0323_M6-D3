# EPICODE WDPT0323 M6 D3

> Esegui le seguenti query usando MongoCompass

---

- Trova tutte le risorse con il dato `isActive` corrispondente a true:
    - ```js
        {isActive: true}

- Trova tutte le risorse con il dato `age` maggiore di 26:
    - ```js
        {age: {$gt: 26}}

- Trova tutte le risorse con il dato `age` maggiore di 26 e minore o uguale a 30:
    - ```js
        {$and: [{"age": {$gt: 26}},{"age": {$lte: 30}}]}

- Trova tutte le risorse con il dato `eyes` che sia brown o blue:
    - ```js
        {$or: [{eyeColor: "brown"},{eyeColor: "blue"}]}

- Trova tutte le risorse che non presentano il dato `eyes` uguale a green:
    - ```js
        {eyeColor: {$ne: "green"}}

- Trova tutte le risorse che non presentano il dato `eyes` uguale a green e neanche a blue:
    - ```js
        {$and: [{eyeColor: {$ne: "green"}},{eyeColor: {$ne: "blue"}}]}

- Trova tutte le risorse con il dato `company` uguale a *"FITCORE"* e ritorna solo l'email:
    - ```js
        Filter: {company: "FITCORE"}
        Project: {email: 1, company: 1}