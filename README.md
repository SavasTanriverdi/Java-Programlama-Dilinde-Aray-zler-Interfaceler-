# Java-Programlama-Dilinde-Aray-zler-Interfaceler-
Java Programlama Dilinde Arayüzler (Interfaceler)
Java Programlama Dilinde Arayüzler (Interfaceler)

Java programlama dilinde, arayüzler (interfaces), nesnelerin belirli davranışları nasıl uygulayacağını tanımlayan bir yapıdır. Arayüzler, sınıflar arasında belirli bir davranışı paylaşmanın yolu olarak kullanılır ve çoklu kalıtımı desteklerler. Bu makalede, Java'daki arayüzlerin ne olduğunu, nasıl tanımlandığını ve nasıl kullanıldığını anlatacağız.
Arayüz Nedir?

Arayüz, bir sınıfın belirli bir davranışı uygulamasını sağlayan bir sözleşmedir. Yani, bir arayüz belirli metotların (fonksiyonların) imzalarını tanımlar, ancak bu metotların nasıl uygulandığını belirtmez. Arayüzlerin amacı, farklı sınıflar arasında belirli bir davranışın paylaşılmasını sağlamaktır.
Arayüz Nasıl Tanımlanır?

Arayüz tanımlamak için interface anahtar kelimesi kullanılır. İşte basit bir arayüz tanımı örneği:

java------------------------------------------

public interface HareketEdebilir {
    void ileriGit();
    void geriGit();
    void dur();
}
------------------------------------------

Yukarıdaki örnek, HareketEdebilir adında bir arayüz tanımlar. Bu arayüz, ileriGit, geriGit ve dur adında üç metodu içerir. Herhangi bir sınıf bu arayüzü uyguladığında (implemente ettiğinde), bu üç metodu da içermek zorundadır.
Arayüz Kullanımı ve Uygulama

Bir sınıfın bir arayüzü uygulaması için implements anahtar kelimesi kullanılır. İşte arayüz uygulama örneği:

java------------------------------------------

public class Araba implements HareketEdebilir {
    @Override
    public void ileriGit() {
        System.out.println("Araba ileri gidiyor.");
    }

    @Override
    public void geriGit() {
        System.out.println("Araba geri gidiyor.");
    }

    @Override
    public void dur() {
        System.out.println("Araba durdu.");
    }
}
------------------------------------------

Yukarıdaki örnekte Araba sınıfı, HareketEdebilir arayüzünü uyguluyor. Bu nedenle sınıf, arayüzde tanımlanan üç metodu da içermek zorundadır. Metotları uygularken @Override anotasyonu kullanılır.
Çoklu Kalıtım ve Arayüzler

Java, çoklu kalıtımı sınıflar arasında desteklemez, ancak arayüzler yardımıyla çoklu kalıtım benzeri bir yapı oluşturabiliriz. Bir sınıf birden fazla arayüzü uygulayabilir. İşte bu kavramın örneği:

java------------------------------------------

public interface Surulebilir {
    void hareketEt();
}
------------------------------------------
public class Kamyon implements HareketEdebilir, Surulebilir {
    // ...
}

Yukarıdaki örnekte Kamyon sınıfı, hem HareketEdebilir hem de Surulebilir arayüzlerini uyguluyor.
