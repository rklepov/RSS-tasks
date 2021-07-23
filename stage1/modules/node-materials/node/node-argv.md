## Аргументы командной строки
В Node.js есть возможность запустить файл с определёнными параметрами. При запуске файла параметры указываются после его имени. Например,   
```node test 1 2 3```  
"1", "2", "3" - это параметры.
Как получить доступ к указанным при запуске файла параметрам? Для этого используется свойство глобального объекта `process` - `process.argv`

В файле `test.js` напишем код  
```console.log(process.argv);```  
В терминале выполним команду `node test 1 2 3`.  
В консоли отображается массив, первые два элемента которого - путь к файлу node.exe и путь к файлу приложения. Дальше идут переданные аргументы.

Если нужно получить только аргументы, выполним код  
```console.log(process.argv.slice(2));```  
Метод `slice(2)` возвращает новый массив, который начинается с элемента с индексом "2".

#### Флаги
Чтобы иметь возможность отправлять аргументы в любом порядке или пропускать какие-то из них, аргументы командной строки можно пометить. Для этого используются флаги - слова или символы, которые указывают, что за ними следует аргумент командной строки. Перед флагами, как правило, ставят один или два дефиса, чтобы не перепутать их с аргументами. Например,  
```node test -m Hello```  
Чтобы получить аргумент с указанным флагом, напишем код  
```js
const index = process.argv.indexOf('-m');
if(index > -1) {
  const message = process.argv[index+1];
  console.log(message);
}
```
Можно этот код преобразовать в функцию, получающую флаг аргумента и возвращающую его значение
```js
function getValue(flag) {
  const index = process.argv.indexOf('-m');
  return (index > 0) ? process.argv[index+1] : null;
}
const message = getValue('-m');
```

## Задание
Напишите программу, которая просит у пользователя ввести два числа, складывает эти числа, если запускается с флагом '-s', или перемножает, если запускается с флагом '-m' и завершает свою работу. Для ввода и вывода информации используйте стандартные потоки ввода/вывода

<details>
<summary>Решение</summary>


```js
  const stdout = process.stdout;
  const stdin = process.stdin;
  const flag = process.argv[2];
  
  stdout.write('Введите, пожалуйста, два числа\n');
  stdin.on('data', data => {
    const arr = data.toString().split(' ');
    const sum = arr.reduce((a, b) => +a + +b);
    const multiple = arr.reduce((a, b) => +a * +b);
    if(arr.length === 2 && flag === '-s') {
      stdout.write(`${+arr[0]} + ${+arr[1]} = ${sum}`);
    } else if(arr.length === 2 && flag === '-m') {
      stdout.write(`${+arr[0]} * ${+arr[1]} = ${multiple}`);
    } else {
      stdout.write('Попробуйте ещё раз запустить файл с флагом -s или -m');
    }
    process.exit();
  });
```

</details>