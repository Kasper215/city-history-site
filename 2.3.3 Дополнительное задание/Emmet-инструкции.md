# 2.3.3 Дополнительное задание

Для каждой страницы ниже приведена одна комбинированная Emmet-инструкция. Она показывает общую оболочку сайта и основную семантическую структуру раздела. Кратность `*n` задаёт повторяющиеся элементы.

Разверните инструкцию в соответствующем HTML-файле и сравните полученную структуру с текущей разметкой страницы.

## Главная — `index.html`

```emmet
html:5>body#top>(a.skip-link)+(header.site-header>div.container.header-inner>(a.brand>span.brand-mark+span>small)+(nav.site-nav[aria-label="Основная навигация"]>a*6))+main#main-content>(section.hero.container[aria-labelledby="hero-title"]>(div.hero-copy>p.eyebrow+h1#hero-title+p.hero-lead+div.hero-stats>div*2)+div.hero-visual>img+div.photo-label)+(section.container.section-pad>(div.section-heading>(div>p.eyebrow+h2#gallery-title)+p.section-aside)+(div.photo-grid>figure.photo-card*5>img+figcaption)+p.photo-credit)+(section.event-section>div.container>(div>p.eyebrow+h2+p+a.button)+(aside.event-card>p.event-kicker+h3+p+time+a+small))+(section.container.section-pad.feature-row>div>p.eyebrow+h2+a.feature-link*3))+footer.site-footer>div.container.footer-inner>a.brand+p+a.back-top+a.floating-top
```

## История — `history.html`

```emmet
html:5>body#top>(a.skip-link)+(header.site-header>div.container.header-inner>(a.brand>span.brand-mark+span>small)+(nav.site-nav[aria-label="Основная навигация"]>a*6))+main#main-content.container.inner-page>(section.page-hero>p.eyebrow+h1+p.hero-lead)+(section.history-intro>(article.history-story>figure.history-photo>img+figcaption+p.eyebrow+h2+p*2+blockquote)+aside.history-note>strong+span)+(section.timeline-section>(div.section-heading>(div>p.eyebrow+h2)+p.section-aside)+(div.table-wrap>table>caption+(thead>tr>th*3)+(tbody>tr*12>(th[scope="row"]>time)+td*2))+(details.source-note>summary+p))+footer.site-footer>div.container.footer-inner>a.brand+p+a.back-top
```

## Город — `infrastructure.html`

```emmet
html:5>body#top>(a.skip-link)+(header.site-header>div.container.header-inner>(a.brand>span.brand-mark+span>small)+(nav.site-nav[aria-label="Основная навигация"]>a*6))+main#main-content.container.inner-page>(section.page-hero>p.eyebrow+h1+p.hero-lead)+(section.geo-grid>article.geo-card*2>span.card-index+h2+p+dl.facts-list>div*3>dt+dd)+(section.map-section>(div.section-heading>(div>p.eyebrow+h2)+p.section-aside)+(div.map-frame>iframe)+p.map-caption)+(section.transport-section>(div>p.eyebrow+h2+p*2)+(div.transport-list>article*3>span+div>h3+p))+footer.site-footer>div.container.footer-inner>a.brand+p+a.back-top
```

## Культура — `culture.html`

```emmet
html:5>body#top>(a.skip-link)+(header.site-header>div.container.header-inner>(a.brand>span.brand-mark+span>small)+(nav.site-nav[aria-label="Основная навигация"]>a*6))+main#main-content.container.inner-page>(section.page-hero>p.eyebrow+h1+p.hero-lead)+(section.culture-feature>(figure.culture-image>img+figcaption)+(article.culture-copy>p.eyebrow+h2+p*2+details>summary+ul>li*4))+(section.culture-cards>article*3>span.card-index+h3+p+a)+(section#event.event-detail>(div.event-date>span+small)+(div>p.eyebrow+h2+p+a))+(section#sources.sources>h2+p*2)+footer.site-footer>div.container.footer-inner>a.brand+p+a.back-top
```

## Разработчик — `about.html`

```emmet
html:5>body#top>(a.skip-link)+(header.site-header>div.container.header-inner>(a.brand>span.brand-mark+span>small)+(nav.site-nav[aria-label="Основная навигация"]>a*6))+main#main-content.container.inner-page>(section.page-hero>p.eyebrow+h1+p.hero-lead)+(section.profile-layout>(figure.profile-photo-wrap>img.profile-photo)+(article.profile-copy>p.eyebrow+h2+p.profile-meta+p*2+h3.skills-heading+(div.skill-list>div.skill-row*4>(div>strong+span)+(div.skill-track>meter[min="0"][max="100"][value]))+aside.project-status>label+progress#project-progress[value="6"][max="6"]+span+a.button))+footer.site-footer>div.container.footer-inner>a.brand+p+a.back-top
```

## Обратная связь — `contact.html`

```emmet
html:5>body#top>(a.skip-link)+(header.site-header>div.container.header-inner>(a.brand>span.brand-mark+span>small)+(nav.site-nav[aria-label="Основная навигация"]>a*6))+main#main-content.container.inner-page>(section.page-hero>p.eyebrow+h1+p.hero-lead)+(section.contact-layout>(div.contact-note>p.eyebrow+h2+p+address>strong+br+br)+(form.contact-form[aria-describedby="form-status"]>(div.form-field>label+input+small)+(div.form-field>label+input+small)+(div.form-field>label+select)+(div.form-field>label+textarea+small)+button.button.button-dark[disabled]+p#form-status.fine-print))+footer.site-footer>div.container.footer-inner>a.brand+p+a.back-top
```


## SCSS

Исходник [`scss/styles.scss`](../scss/styles.scss) содержит переменные, миксины, наследование и правила с вложенностью по компонентам. Сборка из корневой папки проекта:

```powershell
npm run build:all-css
```

Результат записывается в `css/styles.css`, который подключён во всех основных HTML-страницах: браузер загружает скомпилированный CSS, а SCSS остаётся исходником.


