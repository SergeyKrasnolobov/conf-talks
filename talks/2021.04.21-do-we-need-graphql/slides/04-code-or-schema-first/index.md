# Code-first

# или

# Schema-first?

-----

## Я [тут давеча узнал](https://youtu.be/HMTIUQPAbRs), что в моём мире эти понятия немножко извращены

# 😳

-----

### Общепринятый взгляд <br/> (со стороны разработки любого API) <!-- .element: class="gray" -->

<https://swagger.io/blog/api-design/design-first-or-code-first-api-development/> <!-- .element: style="font-size: 0.7em;" class="gray" -->

### Schema-first (Design First) <!-- .element: class="fragment orange" style="margin: 30px 0 0 0;" -->

- When Developer Experience Matters <!-- .element: class="fragment" -->
- When Delivering Mission Critical APIs <!-- .element: class="fragment" -->
- When Ensuring Good Communication <!-- .element: class="fragment" -->

### Code-first <!-- .element: class="fragment orange" style="margin: 30px 0 0 0;" -->

- When Delivery Speedy Matters <!-- .element: class="fragment" -->
- When Developing Internal APIs <!-- .element: class="fragment" -->

-----

### Мой же извращенный взгляд <br/>(со стороны написания первого GraphQL API) <!-- .element: class="gray" -->

### Schema-first <!-- .element: class="fragment orange"  style="margin: 30px 0 0 0;" -->

- это значит взять graphql-tools и объявить схему через SDL <!-- .element: class="fragment" -->
- какое нафиг проектирование, сперва надо заставить эту штуку хоть как-то заработать <!-- .element: class="fragment" -->

### Code-first <!-- .element: class="fragment orange" style="margin: 30px 0 0 0;" -->

- это взять готовые модели и с них "правильно" сгенерировать GraphQL-типы <!-- .element: class="fragment" -->
- например генерировать Input-типы, если они по структуре одинаковы с Output-типами <!-- .element: class="fragment" -->

-----

### Мой взгляд в правильной терминологии <!-- .element: class="gray" -->

### SDL First (graphql-tools) <!-- .element: class="fragment green"  style="margin: 30px 0 0 0;" -->

- Быстрый старт для новичка (если не паримся на дизайне) <!-- .element: class="fragment" -->
- Для маленьких и средних приложений. На длинной дистанции, проблемы с внесением изменений (опечатки, синхронизация Input/Output-типов). <!-- .element: class="fragment" -->

### Generator first <!-- .element: class="fragment green" style="margin: 30px 0 0 0;" -->

- Долго стартуем с поиском/написанием генератора для себя <!-- .element: class="fragment" -->
- На длинной дистанции, меняем логику генератора и наша схема быстро меняется вне зависимости от кол-ва моделей (без опечаток и проблем синхронизации типов) <!-- .element: class="fragment" -->

-----

Если у вас гексагональная (или луковая) архитектура, есть DTO, куча интерфейсов, портов и адаптеров, увлекаетесь рефлексией и декораторами, то однозначно надо брать `Generator first`.

Зачем писать GraphQL-схему ручками через SDL First, когда у вас достаточно артефактов, чтобы ее `сгенерировать`?!

-----

А уже ваш `генератор` должен быть спроектирован так, чтобы следовать какому-то строгому дизайну <br />(принципам которые вы бы заложили в Schema-first, <br/>описывая схему руками).

-----

#### Другими словами: <!-- .element: class="gray" -->

### Я за Schema-first, где бо́льшую часть работы делает code.
## Я за schema-code-first! <!-- .element: class="fragment green" -->

# 🐓🥚 <!-- .element: class="fragment" -->
