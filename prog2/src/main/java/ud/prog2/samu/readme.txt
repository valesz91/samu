// Futtatni a szokásos módon tudod: javac-al compile, utána java-val futtatás.
// A link grammar miatt viszont kell még egy kis plusz:
//
// sudo ln -sv "$(pwd)/link-grammar/.libs/liblink-grammar.so.5" /usr/lib/
//
// sudo ln -sv "$(pwd)/bindings/java-jni/.libs/liblink-grammar-java.so" /usr/lib/
//
// Ezt a két parancsot add ki, abban a mappában ahova letöltötted a link-grammart még anno.
// Pl nálam ez a /home/bszabo/link-grammar-5.2.5/ könyvtárban volt. Ez egy szimbolikus linket rakna be (duh).
// De ha már létezne a liblink-grammar.so.5 és a liblink-grammar-java.so akkor nyugodtan töröld ki őket, és aztán add ki megint a parancsot.
//
// Ezek után akkor fordítás:
//
// javac -cp /home/bszabo/link-grammar-5.2.5/bindings/java/linkgrammar-5.2.5.jar *.java
//
// (értelemszerűen a cp után a saját link grammar mappádat írd, és azon belül a bindings/java/linkgrammar-vmennyi.jar-t
//
// Majd a futtatás:
//
// java -cp /home/bszabo/link-grammar-5.2.5/bindings/java/linkgrammar-5.2.5.jar:`pwd` Main
//
// (itt megint változhat nálad a link-grammar..., ha megcsináltad a simbolikus linkeket a :`pwd` ne maradjon le a végéről)
//