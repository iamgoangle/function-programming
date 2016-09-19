# functional-programming
Learning about function programming via JS language

# ความเป็นมา

เริ่มแรกเดิมทียังไม่รู้จัก FP หรือ Functional Programming จนมาจับ React JS และจำเป็นต้องใช้ Redux ในการจัดการ State
[Redux](http://redux.js.org/) เจ้าตัวนี้เข้ามาจัดการ props, state ของ React JS ให้ดีขึ้น โดยมันจะแบ่งออกเป็น สามงานหลักๆ ได้แก่ Store, Action and Reducer รายละเอียดเพิ่มเติมหาได้ใน google หรือ [http://www.somkiat.cc/redux-for-mobile-application/](http://www.somkiat.cc/redux-for-mobile-application/) ซึ่งอธิบายได้ดี

หนึ่งใน redux princicle คือ Changes are made with pure function

ก็ไปสืบค้นข้อมูลต่อว่า pure function คืออะไร?

จนมาเจอกับคำว่า Mutable and Immutable

กฏของ Reducer คือ We don't mutate the state (Reducers are just pure functions that take the previous state and an action, and return the next state. Remember to return new state objects) และ We return the previous state in the default case

ดังนั้นตอนนี้ มีเรื่องที่ต้องศึกษา ดังนี้
1. Mutate
2. Immutate
3. Imperative Programming
4. Functional Programming
5. Pure Function

# สรุป

## Functional Programming
1. จำนวน Output ของ function จะสอดคล้องกับจำนวน Input เสมอ
2. ต้องเป็น Immutate เสมอ นั่น คือ การนำ Input ของ parameter ไปใช้ใน ฟังก์ชั่น จะต้องไม่ส่งผลกระทบกับ ค่าข้อมูลต้นทาง ไม่ว่าจะเกิดการเปลี่ยนแปลงใดๆ หรือ การเปลี่ยนแปลง state ใดๆ จะต้องส่งผลลัพธ์ในฐานะ state ใหม่ แทนที่จะเขียนทับ state เก่า แล้วส่งออกไป
3. ห้ามเป็น Mutate หรือ Mutation ซึ่งมันตรงข้ามกับ Immutate โดยสิ้นเชิง สถานะการณืสมมุติ เช่น มี Array 1 ชุด ส่งเข้าไปใน หนึ่ง function เพื่อทำการวนลูป push() การทำแบบนี้จะส่งผลถึง state ต้นทางด้วย ตัวอย่าง Array mutation [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array#Mutator_methods](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array#Mutator_methods)
4. Pure function คืออะไร ? เป็นผลลัพธ์ของการทำ Immutate state ฟังก์ชั่นใดก็ตามที่ทำลักษณะนี้ได้ ถือว่าเป็น Pure function ไม่มีสิ่งเจือปน ไม่ยุ่งกับ state ก่อนหน้า ไม่เปลี่ยน แต่สร้าง state ใหม่ที่เพิ่ม เติม หรือ ลดจาก state เก่า
5. First class function คือ feature ที่สนับสนุนให้ฟังก์ชั่น เป็นพลเมืองอันดับหนึ่ง เทียบเท่ากับ Variable ในภาษานั้นๆ ดังนั้น เราสามารถจับ function เข้าไปเป็นตัวแปรได้ เช่น `const a = function () {} or const a = () => {}`
6. Higher order function คือ เราสามารถส่งฟังก์ชั่น เข้าไปเป็นส่วน Argument ของฟังก์ชั่นอื่นได้ และ return function ออกมา

# Referrences
1. [https://medium.com/funk-tional/hello-functional-programming-eacb0091a53c#.4zhercqrm](https://medium.com/funk-tional/hello-functional-programming-eacb0091a53c#.4zhercqrm)
2. [https://medium.com/@imkrish.developer/%E0%B9%81%E0%B8%A5%E0%B8%B0%E0%B9%81%E0%B8%A5%E0%B9%89%E0%B8%A7%E0%B9%80%E0%B8%A3%E0%B8%B2%E0%B8%81%E0%B9%87%E0%B8%AD%E0%B8%A2%E0%B8%B2%E0%B8%81%E0%B9%80%E0%B8%9B%E0%B9%87%E0%B8%99-functional-programmer-%E0%B8%95%E0%B8%AD%E0%B8%99%E0%B8%97%E0%B8%B5%E0%B9%88-1-purity-8f6b934f4dbc#.8v7m5q2ng](https://medium.com/@imkrish.developer/%E0%B9%81%E0%B8%A5%E0%B8%B0%E0%B9%81%E0%B8%A5%E0%B9%89%E0%B8%A7%E0%B9%80%E0%B8%A3%E0%B8%B2%E0%B8%81%E0%B9%87%E0%B8%AD%E0%B8%A2%E0%B8%B2%E0%B8%81%E0%B9%80%E0%B8%9B%E0%B9%87%E0%B8%99-functional-programmer-%E0%B8%95%E0%B8%AD%E0%B8%99%E0%B8%97%E0%B8%B5%E0%B9%88-1-purity-8f6b934f4dbc#.8v7m5q2ng)
3. [https://medium.com/@adakaminkure/chapter-0-introduction-%E0%B8%81%E0%B9%88%E0%B8%AD%E0%B8%99%E0%B8%88%E0%B8%B0%E0%B9%80%E0%B8%A3%E0%B8%B4%E0%B9%88%E0%B8%A1%E0%B8%A5%E0%B8%B8%E0%B8%A2%E0%B8%81%E0%B8%B1%E0%B8%99-37464f4ff3b6#.88h8wn410](https://medium.com/@adakaminkure/chapter-0-introduction-%E0%B8%81%E0%B9%88%E0%B8%AD%E0%B8%99%E0%B8%88%E0%B8%B0%E0%B9%80%E0%B8%A3%E0%B8%B4%E0%B9%88%E0%B8%A1%E0%B8%A5%E0%B8%B8%E0%B8%A2%E0%B8%81%E0%B8%B1%E0%B8%99-37464f4ff3b6#.88h8wn410)
4. [https://medium.com/@cscalfani/so-you-want-to-be-a-functional-programmer-part-1-1f15e387e536#.7qpwmoue6](https://medium.com/@cscalfani/so-you-want-to-be-a-functional-programmer-part-1-1f15e387e536#.7qpwmoue6)
