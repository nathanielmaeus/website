---
title: Оптимизация SVG элементов
date: 2020-07-08T22:01:00.000Z
lang: 'ru'
tags: react svg
cover: https://res.cloudinary.com/dk4mytxmk/image/upload/f_auto,q_auto,w_1100/v1596055810/website/carbon_2_l396bg.jpg
---

SVG элементы достаточно эффективны и очень часто используются для различных нужд в проектах. Как правило, в React каждому SVG элементу соответствует React компонент, который уже потом импортируется в нужное место.
Очень часто разработчики получают от дизайнеров неоптимизированный элемент и незамедлительно добавляют их в свой код. Как итог, за счет такого невнимательного отношения
размер вашего приложения может увеличиться на десятки килобайт.

Это скажется на времени загрузки приложения, а следовательно и на удобстве его использования на устройствах со слабым интернетом.
Поэтому в таких случаях я пользуюсь специальным сервисом для SVG элементов, который позволяет оптимизировать такие изображения за счет уменьшения описания SVG фигур путем упрощения их координат и схлопывания различных внутренних элементов. Например, [SVGOMG](https://jakearchibald.github.io/svgomg/) позволит оптимизировать размер ваших иконок. Более того в нем очень удобно настроить это оптимизацию благодаря различных ползункам настроек.

<picture>
    <source media="(max-width: 767px)" 
            sizes="1px"
            srcset="https://res.cloudinary.com/dk4mytxmk/image/upload/w_0.5,q_auto,f_auto/v1596141089/website/svgo_zyhlo7.jpg" />
    <source media="(min-width: 768px)" 
            sizes="300px" 
            srcset="https://res.cloudinary.com/dk4mytxmk/image/upload/v1595920880/website/svgo_zyhlo7.jpg" />
    <img src="https://res.cloudinary.com/dk4mytxmk/image/upload/v1595920880/website/svgo_zyhlo7.jpg" alt="SVGOMG webview" loading="lazy" />
</picture>

Еще один сервис [svg2jsx](https://svg2jsx.com/) позволяет пробразовывать SVG элемент в валидный для React код. Это очень удобно, когда SVG элемент использует свойства в виде kebab-case. Чтобы JSX правильно вадидировал эти свойства сервис автоматически преобразует их в camelCase, который удобоварим для React.

<picture>
    <source media="(max-width: 767px)" 
            sizes="1px"
            srcset="https://res.cloudinary.com/dk4mytxmk/image/upload/w_0.5,q_auto,f_auto/v1595920880/website/svgomg_oxpfgj.jpg"/>
    <source media="(min-width: 768px)" 
            sizes="300px" 
            srcset="https://res.cloudinary.com/dk4mytxmk/image/upload/v1595920880/website/svgomg_oxpfgj.jpg" />
    <img src="https://res.cloudinary.com/dk4mytxmk/image/upload/v1595920880/website/svgomg_oxpfgj.jpg" alt="SVG2jsx webview" loading="lazy" />
</picture>

И последний самый удобный сервис — [transform](https://transform.tools/). Помимо возможностей преобразования различных форматов на все случаи жизни (например, мое любимое — преобразование JSON в Typescript) так же имеет оптимизацию SVG изображений и совмещает в себе оба вышеперечисленных сервиса.

<picture>
    <source media="(max-width: 767px)" 
            sizes="1px"
            srcset="https://res.cloudinary.com/dk4mytxmk/image/upload/w_0.5,q_auto,f_auto/v1596737668/website/transform_ftkbby.jpg"/>
    <source media="(min-width: 768px)" 
            sizes="300px" 
            srcset="https://res.cloudinary.com/dk4mytxmk/image/upload/v1596737668/website/transform_ftkbby.jpg" />
    <img src="https://res.cloudinary.com/dk4mytxmk/image/upload/v1596737668/website/transform_ftkbby.jpg" alt="Transform webview" loading="lazy" />
</picture>
