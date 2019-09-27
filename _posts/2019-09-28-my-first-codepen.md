---
layout: post
title: บันทึกครั้งแรกกับการเขียน CodePen
date: 28-09-2019 00:03:00
tags: [webdev]
---

 ไม่ได้เขียนบล็อกมานานมาก (มากกกกกกจริงๆ) บล็อกล่าสุดเขียนเมื่อเกือบสองปีก่อน 5555 พอดูเวลาของบล็อกแรกก็พบว่าเฮ้ย เราทิ้งบล็อกไว้บน GitHub Pages มาจะสี่ปีแล้วนะ ช่วงนี้กำลังพยายามหาเวลามาจัดการกับสิ่งที่ติดค้างอยากทำมานาน และนี่ก็เป็นหนึ่งในสิ่งที่อยากทำ นั่นก็คือการเขียน CodePen ของตัวเองบ้างซะที

 ที่ผ่านมาเราก็ได้ใช้บริการ (ส่องโค้ดคนอื่น) พวกนี้มาตลอด ทั้ง CodePen, CodeSandbox หรือ JSFiddle แต่ก็ไม่เคยจะมีจังหวะมาเขียนอะไรที่เกิดจากไอเดียตัวเองจริงๆ ซะที มาวันนี้โอกาสดี มีสิ่งที่อยากทดลองจากโปรเจ็คนึงที่ทำอยู่ก็เลยทำซะเลย

 Pen นี้แค่อยากลองว่าเราจะสามารถเซตสีพื้นหลังของไอคอนจาก FontAwesome ให้มันเพิ่มขึ้นเป็น % ได้มั้ย ลองค้นๆ ดูก็เจอคนทำด้วยวิธีที่เราเองก็คิดแว๊บแรกเมื่อเจอโจทย์นี้ เช่น วาดไอคอนขึ้นมาสองอันทับกัน กำหนดขนาดของอันแรกแล้วซ่อนส่วนเกินด้วย `overflow: hidden` แต่คิดไปคิดมา gradient ก็น่าจะทำได้นี่หว่า ก็เลยลองไปตามนั้น

 สำหรับ Environment นั้นเราชอบ React กับ styled-components มากๆ แต่เนื่องจากไม่เคยใช้ CodePen มาก่อน เลยเสียเวลางมว่ามัน import ยังไงไปสักพักใหญ่ๆ แต่พอเริ่มคุ้นแล้วก็เพลินเลย จบบล็อกนี้ไปเท่านี้เลยดีกว่า ปิดท้ายกันด้วย Pen โลด

<p class="codepen" data-height="406" data-theme-id="dark" data-default-tab="js,result" data-user="bluenex" data-slug-hash="oNvOZJY" data-preview="true" style="height: 406px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="star-dynamic-color">
  <span>See the Pen <a href="https://codepen.io/bluenex/pen/oNvOZJY">
  star-dynamic-color</a> by Tulakan Ruangrong (<a href="https://codepen.io/bluenex">@bluenex</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>
