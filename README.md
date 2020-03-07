<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title>День рождения</title>
  </head>
  <body>

    <script>
      // Создаем чат бота
      alert('Привет! Я - ваш компьютер.');
      var name = prompt('Как вас зовут?');
      alert('Отлично ' + name + ', приятно познокомится!');
      var hobby = prompt('Скажите, ' + name + ', а какое у вас хобби?');

      alert('Действительно, ' + hobby + ' - интересное занятие! А я больше всего люблю вычисления и алгоритмы');
      var d = prompt(name + ' у меня для вас сюрприз! Напишите свой день рождения в формате месяц-день (например, 05-23)');

      // Началась магия, где мы берем текущую дату и сравниваем с тем, что вы ввели
      var current_date = new Date();
      var my_date = new Date ( (d + '-' + (current_date.getFullYear()+1)) );
      var dayZ = Math.abs( (( Date.parse(my_date) - Date.parse(current_date))/(1000*3600*24)) % 365);
      var result = dayZ.toFixed(0);
      // Магия закончилась, в переменной result у нас теперь хранится кольчесво дней

      alert('Знаете сколько дней осталось до вашего дня рождения? ' + result + ' дня(ей)!');
      alert('Спасибо за общение, ' + name + ', еще увидимся!');

    </script>
  </body>
</html>
