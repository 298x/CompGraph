# Lab 1
>Код в файле ComputerGraphics-1.cpp 

#### Основные функции:
* `glutInit(&argc, argv);` - Инициализация GLUT
* `glutInitDisplayMode(GLUT_DOUBLE | GLUT_RGBA);` - Включение двойной буферизации и буфера цвета
* `glutInitWindowSize(1024, 768);` - Размер окна
* `glutInitWindowPosition(100, 100);` - Положение окна
* `glutCreateWindow("Window");` - Создание окна
* `glutDisplayFunc(RenderSceneCB);` - Вызов функции отображения на экран
* `glClearColor(0.4f, 0.0f, 0.0f, 0.0f);` - Установка цвета, которой будет использоваться во время очистки буфера кадра
* `glutMainLoop();` - Передача контроля GLUTу
  
* `GLenum res = glewInit();`- Инициализация glew
* `GLuint VBO;` - Указатель VBO на буфер вершин
* `glGenBuffers(1, &VBO);` - Генерация объектов
* `glBindBuffer(GL_ARRAY_BUFFER, VBO);` - Цель использованиея буферов - хранит массив вершин
* `glBufferData(GL_ARRAY_BUFFER, sizeof(Vertices), Vertices, GL_STATIC_DRAW);` - Наполнение объекта нужными данными *GL_STATIC_DRAW - флаг, обозначающий исп. паттернов для этих данных*
* `glClear(GL_COLOR_BUFFER_BIT);` - Очистка буфера кадра
* `glVertexAttribPointer(0, 3, GL_FLOAT, GL_FALSE, 0, 0);` - Говорим конвейеру, как воспринимать данные внутри буфера
* `glDrawArrays(GL_POINTS, 0, 1);` - Вызываем функцию отрисовки точки
* `glDrawArrays(GL_TRIANGLES, 0, 3);` - Вызываем функцию отрисовки треугольника
* `glDisableVertexAttribArray(0);` - Отключение атрибутов вершины
* `glutSwapBuffers();` - Сменя буфера фона на буфер кадра
  
