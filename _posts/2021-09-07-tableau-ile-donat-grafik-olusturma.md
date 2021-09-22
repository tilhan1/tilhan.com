---
layout: post
title:  "Tableau ile Donat Grafik"
language: tr
date:   2021-09-07
author: Tayip
categories: [Tableau]
excerpt: "Tableau ile Donat Grafik oluşturma"
image: "assets/images/donut.png" 
tags: [Tableau, Desktop, Donat, Grafik, ]
beforetoc: "Tableau ile Donat Grafik oluşturma"
toc: false
---
## Tableau Desktop ile Donat Grafik Oluşturma

Selamlar. Bu yazımda Tableau Desktop ile Donat Grafik oluşturmaktan bahsedeceğim.

Öncelikle bu konuyu Tableau Sample - Superstore verisi üzerinden anlatacağım. Örnek veriyi açıp Sayfa 1'e geçiyorum. Sayfanın varsayılan tipini Pie (Pasta) grafik olarak değiştiriyorum ve sayfa görünümünü Entire View (Tüm Görünüm) olarak değiştiriyorum. Ardından Columns (kolon) sekmesine 2 adet sum(0) ekliyorum. Böylece sayfayı ikiye bölüp Marks (İşaretçiler) altında iki farklı sekme oluşturuyorum. Sum(0) ile oluşturduğum sekmelerden ilkine tıklayıp SuperStore verisinde bulunan Sales verisini Angle (Açı) kutucuğunun üzerine sürükleyip bırakıyorum. Böylece verinin içerisinde bulunan değerler birazdan ekleyeceğim kırılıma göre pasta grafikten kendi değerlerini alacaklar. Grafiğimi görselleştirmek için Segment verisini Color (Renk) kutucuğunun içerisine bırakıyorum. Böylece Segment verisinde bulunan 3 farklı veriye göre pasta grafiğim 3 eşit parçaya ayrılıyor. Bu parçaları büyüklüğüne göre boyutlamak için yine Sales verisini Size (Boyut) kutucuğunun içerisine bırakıyorum. Ve Size kutucuğuna tıklayıp boyutunu biraz büyütüyorum. Şimdi ikinci Sum(0) kutucuğuna tıklayıp Color kutucuğuna tıklıyorum ve beyaz rengini seçiyorum. Ardından Columns da bulunan Sum(0) lardan birine sağ tıklayıp Dual Axis seçeneğine tıklıyorum. Artık beyaz olarak verdiğim Sum(0) üste gelecek ve alttaki pasta grafik aslında donut grafiğe dönüşecek.

Not:  Sum(0) lardan gelen axis çizgilerini kaldırmayı unutmayın.