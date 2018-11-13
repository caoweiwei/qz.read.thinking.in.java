1. static关键字中所周知会随者类的加载而加载，但是有时候代码的表象可能会让你有错误的认识
    例如：

            public class A {
                public static final int NUM = 1;

                static {
                    print("hello world A");
                }
            }

            public class B {
                public static final Date DATE = new Date();

                static {
                    print("hello world B");
                }
            }

            public static void main(String[] args) {
                print(A.NUM);
                print(B.DATE);
            }
     像上面这个例子，第一反应就是两个静态代码块中的hello world A和hello world B都会执行打印，但是事实不是这样的。hello world A不会打印hello world会打印。

     *因为A.NUM是调用的基本类型，此时编译器会直接把基本类型的NUM直接在编译期间进行常量替换，print(A.NUM);生成的class字节码文件会变成print(1); 所以这个过程并没有加载A类，所以A
     的静态代码块就不会执行了，而B.DATE是运行时的操作，必然涉及到B类的加载，所以B类的静态代码块会执行*

