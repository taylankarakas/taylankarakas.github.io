---
layout: post
title:  "Nedir bu react.js ?"
description: "React Series"
date: 2019-03-10
tags: [React, Development, Frontend, App]
categories: [Be Hungry For Learning]
reading_time: "3-4 min."

---

>Programlama, günlük hayatta karşılaştığımız problemleri makineler ile çözmek istediğimizde öncelikle problemi makineye aktarmak, çözüm yolları sunmak ve sunulan bu çözüm yolları ile bir sonuca ulaşmak aşamalarını barındıran bir tekniktir.

![Programming Languages](https://www.muhendisarsivi.com/wp-content/uploads/2017/03/programlama-dilleri-1.jpg)

Makineler, bahsettiğimiz bu aşamaları anlayabilmek için konuştuğumuz dilden farklı bir dile ihtiyaç duyarlar. Bu diller programlama dilleridir. Dünya üzerinde amaçlarına göre birçok programlama dili mevcuttur. Fakat bizim burada React için konuşmamız gereken programlama dili Javascript’ tir.

>Javascript dili, 1995 yılının Mayıs ayında Brendan Eich tarafından geliştirilmiştir.
Orjinal adı Mocha’ ydı. Eylül 1995’ te LiveScript ve yine o yılın son ayında Javascript adını almıştır.
Javascript; 1996-1997 yıllarında,  gelişen bilgi teknolojilerinin kontrolünün ve bu teknolojilerin birbirlerine uyumunun zorlaşması sorununa odaklanan, Dünya Uluslararası Standartları Kurumu’ ndan olan ECMA tarafından ele alınmıştır. 
Sonrasında ECMAScript resmi standart ismini almıştır. Günümüzde ise ECMAScript 6 (ES6) ve ECMAScript 7 (ES7 - Tarayıcı desteği henüz tamamlanmamıştır.) güncel versiyonlardır.

![Javascript](http://www.purelogics.net/blog/wp-content/uploads/2019/01/javascript.png)

Temel bilgilerin ardından asıl konumuz olan React’ a adım atabiliriz. Öncelikle ES6 desteği olduğu için kod yazımı konusunda bizleri rahatlatan React, birçok geliştiricinin söylediğinin aksine bir **Javascript kütüphanesi**'dir. Bir framework olmamasının sebebi, bir framework gibi içerisinde bulundurduğu tasarım desenini bize kod yazarken dayatmıyor olmasıdır. 
	
![React](https://scriptverse.academy/img/tutorials/reactjs-tutorial.png)

React, “**kullanıcı arayüzü oluşturmak için bir Javascript kütüphanesi**” dir. Bu cümleyi okuduktan sonra aklınızda bazı sorular oluşabilir:
*	React’ tan önce kullanıcı arayüzü nasıl oluşturuluyordu?
*	React’ ın ne gibi faydaları var?
*	React’ın diğer kütüphane ya da frameworklerden ne gibi farkı var?
*	Bundan sonra React kullanmak zorunda mıyız?

gibi.

Dilerseniz bu sorulara beraber cevap arayalım. 

React, hepimizin yakından tanıdığı **Facebook** şirketinin bazı ihtiyaçları sonucunda yine Facebook yazılım ekibi tarafından yazılmıştır. Peki bu ihtiyaçlar neydi? Facebook’ un günümüz versiyonlarından önceki versiyonlarını kullanan insanların belki de farkında olmadığı ya da farkında olup da kabullendiği problemleri vardı:
*	Çevrimiçi olan arkadaşlarımızın güncelliğini kontrol edebilmek
*	Anlık gelen mesajın bize ulaşması
*	Anlık bildirim durumu

vb. 

Bahsetmiş olduğum birkaç problemin kullanıcılar tarafından en basit ve akla ilk gelen çözümü sayfa yenilemesi yapmaktı (**refresh**). Ama Facebook gibi büyük bir teknoloji şirketi bu soruna daha iyi çözümler üretmeliydi. Akabinde “Gerçek zamanlı (**runtime**) güncellenen web siteleri geliştirmek bu kadar zor olmamalı! ” yaklaşımı ile React gibi bir çözüm üretti. Evet, Facebook interaktif bir web sitesiydi ve bu problemi ortadan kaldırmalıydı.

Bu bilgiden sonra bir adım daha ileriye gidebiliriz.
Bildiğiniz üzere temelde web arayüzü HTML, CSS ve JavaScript’ ten oluşur. 
Bu kavramların yanında çok yabancı olmamamız gereken bir kavram daha var: ‘**DOM**’.

DOM, HTML ile programlama dilleri arasında bir bağ oluşturarak bu dillerin HTML’ den bilgi alıp bilgi vermesine yardımcı olur. HTML’ de yazdığımız her element (tag) bir nesnedir ve DOM, bu nesneleri içerisinde barındırır. Peki DOM ile React’ ın alakası nedir?
	
Bizler HTML yazarken bir elementi başka yerde kullanmamız gerektiğinde yineleme işlemi yaparız. Yani defalarca aynı kodu yazmamız gerekebilir.
React’ ın güzelliklerinden birisi yineleme işlemini ortadan kaldırıp **component** (bileşen) mantığını bize sunmasıdır. Misal biz bir kere ‘<h2>’ componentini oluştururuz ve tekrar tekrar yazmadan istediğimiz yerde istediğimiz kadar kullanabiliriz. Bu kullanım bize daha temiz, daha okunaklı kod yazmamızı ve performans sağlar. Bu biz geliştiriciler açısından önemli bir etkendir.
		
![HTML Tag](http://www.hectormainar.com/sites/default/files/h1_0.jpg)


“DOM ile React’ ın alakası nedir?” in cevabına gelirsek; React, direkt olarak DOM üzerinde değişiklik yapmak yerine gerçek DOM’ un kopyası olan **Virtual DOM** (Sanal DOM) üzerinde değişiklik yapıyor. Diff algoritmaları sayesinde ise Real DOM’ u komple render etmek yerine Sanal DOM ile gerçek DOM’ un karşılaştırmasını yaparak farklılık bulduğu kodda değişiklik yapmaktadır. Bu mantığın faydalı olmasının sebebi yukarıda bahsettiğim gibi performansı olumlu yönde etkilemesidir. Çünkü DOM’ un her **state** (durum) değiştiğinde en baştan tekrar tekrar render edilmesi çok zahmetli bir iştir. 

![React DOM](https://cdn.auth0.com/blog/dombench/reactdom.png)

Araya farklı bir soru alarak “State nedir?” e cevap bulalım. State, componentlerimizin view (görünüm) durumunu belirleyen bir React objesidir.
Yukarıda da anlatmak isyediğim üzere DOM’ un render olması için state’ in değişmesi, state’ in değiştiğini haberdar etmek için de ‘**setstate**’ metodunu çağırmamız gerekmektedir. 

Yeri gelmişken bahsetmemiz gereken iki terim daha bulunuyor, ‘**props**’ ve ‘**lifecycle**’.
Props, componentler arası data (veri) alışverişinde oldukça kolaylık sağlayan bir objedir. **Lifecycle**’lar (yaşam döngüleri) ise biraz derin bir konu olduğu için yüzeysel bahsetmek bu teori kısmı için yeterli olacaktır: DOM’ a müdahale ettiğimiz aşamayı kademelere ayıran yapıdır. Örneğin ‘componentWillMount’, ‘componentDidMount’ vs.

React alternatifleri olabilecek Javascript kütüphane-framework’ lere baktığımızda -tabiki yapacağınız projenin detaylarına göre değişkenlik gösterebilir- öğrenme eğrisinin daha aşağılarda olduğunu rahatlıkla söyeleyebilirim. Bu duruma **React Community**’ sinin (React Topluluğu) etkisinin büyük olmasıyla birlikte kolay alışılabilecek kod yapısı vardır. 

Bu görseli inceleyerek Javascript frameworkü olan Angular ile ReactJS’ in farklarını anlayabilirsiniz.

![Angular](https://mertcangokgoz.com/wp-content/uploads/2018/04/angularjsvereactjsgrafikgorsel1-724x1024.jpg)

Teori aşamasını burada bitirip sonraki yazılarda beraber küçük bir uygulama yapmak istiyorum. Sağlıcakla kalın.

Teşekkürler.

