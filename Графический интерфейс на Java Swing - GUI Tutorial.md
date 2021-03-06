# Swing
В Java есть 2 основных пакета для создания графических интерфейсов (Graphics User Interface). Это Abstract Windows Toolkit (AWT) и Swing. AWT использует виджеты операционной системы, поэтому эта библиотека немного быстрее. Но на мой взгляд, Swing более хорошо спроектирован.

В данном туториале мы рассмотрим основные элементы библиотеки Swing и создадим простой интерфейс (GUI) в качестве примера.

Для группировки компонент интерфейса используются контейнеры (Container). Для создания основного контейнера для приложения чаще всего используется контейнер JFrame (есть еще JWindows и JApplet). Проще всего унаследоваться от JFrame тем самым получить доступ ко множеству методов, например:

setBounds(x, y, w, h) - указывает координаты верхней левой вершины окна, а также его ширину и высоту.

setResizable(bool) - указывает, можно ли изменять размер окна.

setTitle(str) - устанавливает название окна.

setVisible(bool) - собственно отображает окно.

setDefaultCloseOperation(operation) - указывает операцию, которая будет произведена при закрытии окна.

Основные элементы управления:

    JLabel - элемент для отображения фиксированного текста;
    JTextField - простой edit-box;
    JButton - обычная кнопка (button);
    JCheckBox - элемент выбора (аналог checkbox);
    JRadioButton - радио кнопка

Как видите, все довольно просто и логично.

При отображении элементов управления используются специальные менеджеры - LayoutManager. У всех LayoutManager'ов есть методы для добавления у удаления элементов.

FlowLayout - используется для последовательного отображения элементов. Если элемент не помещается в конкретную строку, он отображается в следующей.

GridLayout - отображения элементов в виде таблицы с одинаковыми размерами ячеек.

BorderLayout - используется при отображении не более 5 элементов. Эти элементы располагаются по краям фрейма и в ценрте: North, South, East, West, Center.

BoxLayout - отображает элементы в виде рядка или колонки.

GridBagLayout - позволяет назначать месторасположение и размер каждого виджета. Это самый сложный, но и самый эффективный вид отображения.

Стоит еще обратить внимание на обработку событий. Для этого используются так называемые Event Listeners.

Примечания:

getContentPane возвращает контейнер верхнего уровня. ButtonGroup служит для создания группы взаимосвязанных радио-кнопок.

Внутренний класс ButtonActionListener реализует интерфейс ActionListener. Для этого необходимо предоставить имплементацию метода actionPerformed.

JOptionPane служит для отображения диалоговых окон.
