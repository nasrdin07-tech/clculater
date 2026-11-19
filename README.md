# clculater
calculater mathfuk
class Car {
  constructor(brand, model, year) {
    this.brand = brand;
    this.model = model;
    this.year = year;
    this.speed = 0;
    this.isRunning = false;
  }

  start() {
    if (!this.isRunning) {
      this.isRunning = true;
      console.log(`تم تشغيل السيارة: ${this.brand} ${this.model}`);
    } else {
      console.log("السيارة تعمل بالفعل.");
    }
  }

  accelerate(amount) {
    if (!this.isRunning) {
      console.log("شغّل السيارة أولاً قبل التسريع.");
      return;
    }
    this.speed += amount;
    console.log(`السرعة الحالية: ${this.speed} كم/س`);
  }

  brake(amount) {
    this.speed = Math.max(0, this.speed - amount);
    console.log(`تم تخفيف السرعة إلى: ${this.speed} كم/س`);
  }

  stop() {
    this.speed = 0;
    this.isRunning = false;
    console.log("تم إيقاف السيارة.");
  }
}

// تجربة الكود
const myCar = new Car("Toyota", "Corolla", 2024);
myCar.start();
myCar.accelerate(60);
myCar.brake(20);
myCar.stop();

