# Git ve GitHub'a Giriş

## Git Komutları

### `git init`

- **Açıklama**: Bu komut, yeni bir Git deposu başlatır. Yani, bir projenin takip edilmesi ve sürdürülmesi için bir Git deposu oluşturur.

- **Kullanım**: 
  ```bash
  git init
  ```
  
### `git clone`

- **Açıklama**: Bu komut, uzak bir depoyu (örneğin, GitHub'daki bir repo) yerel bilgisayarınıza klonlar. Yani, uzak bir repo ile yerel bir kopya oluşturur.

- **Kullanım**: 
  ```shell
  git clone [URL]
  ```
  
  Örnek: `git clone https://github.com/kullanici/adiproje.git`

### `git status`

- **Açıklama**: Bu komut, çalıştığınız depo içindeki değişikliklerin durumunu gösterir. Hangi dosyaların değiştirildiğini veya eklenip silindiğini gösterir.

- **Kullanım**: 
  ```shell
  git status
  ```

### `git add`

- **Açıklama**: Bu komut, değişiklikleri Git'in takip edebileceği bir aşamaya (stage) ekler. Yani, değişiklikleri kaydetmek istediğiniz dosyaları belirler.

- **Kullanım**: 
  ```shell
  git add [dosya]
  ```

  Örnek: `git add index.html` (index.html dosyasındaki değişiklikleri ekler)

### `git commit`

- **Açıklama**: Bu komut, stage alanındaki değişiklikleri kalıcı olarak kaydeder. Her commit, bir dizi değişikliği belirli bir noktada kaydeder ve bir mesaj ile açıklanır.

- **Kullanım**: 
  ```shell
  git commit -m "[commit mesajı]"
  ```

  Örnek: `git commit -m "Ana sayfa tasarımını güncelle"`

### `git push`

- **Açıklama**: Bu komut, yerel değişiklikleri uzak bir depoya gönderir. Yani, projenizi uzak sunucuya yükler.

- **Kullanım**: 
  ```shell
  git push origin [dal]
  ```

  Örnek: `git push origin master` (master dalındaki değişiklikleri uzak depoya gönderir)

### `git pull`

- **Açıklama**: Bu komut, uzak bir depodaki değişiklikleri yerel depoya çeker. Yani, projenizin en son halini almanızı sağlar.

- **Kullanım**: 
  ```shell
  git pull origin [dal]
  ```

  Örnek: `git pull origin develop` (develop dalındaki değişiklikleri yerel depoya çeker)

## Git ve GitHub ile İşbirliği

Bu bölümde, Git ve GitHub'ı işbirliği yapmak için nasıl kullanabileceğinizi göreceksiniz.

## GitHub İşbirliği Platformu Olarak Kullanma

- **Açıklama**: GitHub, projelerinizi paylaşmak, işbirliği yapmak ve diğer geliştiricilerle iletişim kurmak için güçlü bir platform sunar. Projelerinizi GitHub'a yükleyerek diğerlerine açık kaynaklı yazılım geliştirme dünyasına katılabilirsiniz.

## Klonlanan Depoların Push Adresini Değiştirme

- **Açıklama**: Klonlanan depoların uzak adresini değiştirmek, genellikle projenin başka bir kopyasını çalıştırmak istediğinizde kullanılır. Örneğin, kendi GitHub hesabınızda bir fork oluşturduysanız ve bu fork'ı klonladıysanız, push adresini fork'unuzun adresine ayarlamak isteyebilirsiniz.

- **Kullanım**: 
  ```shell
  git remote set-url origin [yeni URL]
  ```

  Örnek: `git remote set-url origin https://github.com/kullanici/forked-proje.git`

## Pull Request - Merge Request Nedir

- **Açıklama**: Pull Request (GitHub) veya Merge Request (GitLab) kullanarak, projeye katkıda bulunanların değişikliklerini ana projeye entegre etmek için bir istekte bulunabilirsiniz. Bu, projenizin geliştirilmesine katkıda bulunanların işbirliği yapmasını sağlar.

## Branching Mantığı

- **Açıklama**: Branching, projede bağımsız olarak çalışmayı sağlar ve yeni özellikler veya düzeltmeler üzerinde çalışırken ana kodu etkilemeden deneme yapmanıza olanak tanır.

- **Yeni Dal Oluşturma**: 
  ```shell
  git branch [yeni dal]
  ```

  Örnek: `git branch feature-login` (feature-login adında yeni bir dal oluşturur)

- **Dal Değiştirme**: 
  ```shell
  git checkout [dal]
  ```

  Örnek: `git checkout feature-login` (feature-login dalına geçiş yapar)

## Git Merge - Git Rebase

- **Merge Açıklama**: Git Merge, iki dalı birleştirir ve sonuçta birleştirme commit'i oluşturur. Bu, farklı dallardaki değişiklikleri birleştirmek için kullanılır.

- **Merge Kullanım**: 
  ```shell
  git merge [diğer dal]
  ```

  Örnek: `git merge feature-login` (feature-login dalını mevcut dal ile birleştirir)

- **Rebase Açıklama**: Git Rebase, bir dalın başlangıç noktasını değiştirir. Bu, bir dalı güncellemek veya daha temiz bir commit geçmişi oluşturmak için kullanılır.

- **Rebase Kullanım**: 
  ```shell
  git rebase [dal]
  ```

  Örnek: `git rebase master` (mevcut dalı master dalına göre yeniden baz alır)

##

 Git'te Sık Karşılaşılan Senaryolar ve Çözümleri

Bu bölümde, Git'te sık karşılaşılan sorunlara ve bu sorunları çözme yollarına dair bazı bilgiler bulunmaktadır.

### Geri Alma

- **Kullanım**: 
  ```shell
  git revert [commit hash]
  ```

  Örnek: `git revert abc123` (abc123 commit'ini geri alır)

### Çatışmaların Yönetimi

- **Kullanım**: Çatışmalar, aynı dosyanın aynı satırlarında farklı değişiklikler yapıldığında ortaya çıkar. Çatışma çözmek için aşağıdaki adımları izleyebilirsiniz:
  
  1. İlk olarak, çatışmayı çözmek istediğiniz dosyayı açın ve çatışmayı manuel olarak çözün.
  2. Çatışmayı çözdükten sonra dosyayı kaydedin.
  3. Ardından, aşağıdaki komutları kullanarak çözülen dosyayı stage alanına ekleyin ve commit yapın:
  ```shell
  git add [çözülen dosya]
  git commit -m "Çatışma çözüldü"
  ```

### Uzak Depolarla Çalışma

- **Kullanım**: Uzak depolarla çalışırken, uzak depoların (örneğin GitHub) projenize nasıl ekleyeceğinizi ve bunlarla nasıl etkileşimde bulunacağınızı öğrenmek önemlidir.

  - Uzak Depo Ekleme: 
  ```shell
  git remote add [kısa ad] [URL]
  ```

  Örnek: `git remote add upstream https://github.com/ana-proje/proje.git` (ana projenin uzak depo bağlantısını ekler)

  - Uzak Depo Adlarını Listeleme:
  ```shell
  git remote -v
  ```

  Örnek: `git remote -v` (mevcut uzak depoların adlarını ve URL'lerini listeler)


