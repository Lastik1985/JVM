public class JvmComprehension {

    public static void main(String[] args) {
        int i = 1;                      // 1 переменная i помещается в Stack Memory во фрейм(кадр), созданный под метод main
        Object o = new Object();        // 2 создается объект в "куче"heap, ссылка (o) на данный объект помещается в Stack Memory
        Integer ii = 2;                 // 3 переменная ii помещается в Stack Memory во фрейм под метод main

        printAll(o, i, ii);             // 4 вызывается метод и создается фрейм "printAll" помещаются "o,i,ii"

        System.out.println("finished"); // 7 в ранее созданный фрейм в стэке, передаем строку
    }

    private static void printAll(Object o, int i, Integer ii) {
        Integer uselessVar = 700;                   // 5 в Stack во фрейм "printAll" помещается "uselessVar"
        System.out.println(o.toString() + i + ii);  // 6 создается новый фрейм и в него передается собранная строка
    }
}