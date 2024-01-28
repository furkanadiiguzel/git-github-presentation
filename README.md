# Git ve GitHub'a Giriş


## Git Nedir?

Git, dağıtık bir versiyon kontrol sistemi (VCS) olarak kullanılan açık kaynaklı bir yazılımdır. Git, projelerin sürüm geçmişini ve değişikliklerini takip etmek için kullanılır. Geliştiriciler, kodlarını Git ile yöneterek değişiklikleri izleyebilir, işbirliği yapabilir ve kodlarını güvenli bir şekilde depolayabilirler.

## GitHub Nedir?

GitHub, Git tabanlı projeleri barındırmak, paylaşmak ve işbirliği yapmak için kullanılan popüler bir platformdur. GitHub, kullanıcılara Git deposu barındırma, işlem izleme, Pull Request oluşturma ve diğer birçok işlevselliği sunar. Ayrıca, açık kaynaklı projelerin kolayca katkıda bulunulabileceği bir topluluk platformu olarak da hizmet verir.

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
**Semantic Commit Messages** : https://gist.github.com/joshbuchea/6f47e86d2510bce28f8e7f42ae84c716


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


## Pull Request (GitHub) veya Merge Request (GitLab) Nedir?

Pull Request (PR) veya Merge Request (MR), bir projeye katkıda bulunanların değişikliklerini ana projeye entegre etmek için bir istekte bulunduğu bir işbirliği mekanizmasıdır. Genellikle şu adımları içerir:

1. Kullanıcı, yerel olarak çalıştığı bir dalda (örneğin, "feature-branch") değişiklikler yapar.
2. Yaptığı değişiklikleri, bu dalı uzak bir depoya (GitHub veya GitLab gibi) yükler.
3. Ardından, bu değişiklikleri ana projeye dahil etmek için bir PR veya MR oluşturur.

Projenin sahibi veya diğer katkıda bulunanlar bu isteği inceleyebilir ve gerekirse değişiklikler yapabilirler. Sonunda değişiklikler kabul edilirse, ana projeye dahil edilir.

## Pull Request (PR) veya Merge Request (MR) Nasıl Oluşturulur?

### GitHub için Pull Request Oluşturma

1. GitHub hesabınıza giriş yapın ve projenizin ana sayfasına gidin.
2. Sağ üst köşede "Pull Request" veya "Compare & pull request" düğmesine tıklayın.
3. Karşılaştırılacak iki dalı seçin: karşılaştırmak istediğiniz kendi dalınız (örneğin, "feature-branch") ile ana dal (örneğin, "master").
4. Değişikliklerinizi ve PR ile ilgili detayları ekleyin.
5. PR oluştur düğmesine tıklayarak PR'yi oluşturun.

### GitLab için Merge Request Oluşturma

1. GitLab hesabınıza giriş yapın ve projenizin ana sayfasına gidin.
2. Sağ üst köşede "New Merge Request" düğmesine tıklayın.
3. Karşılaştırmak istediğiniz kendi dalınız (örneğin, "feature-branch") ile hedef dal (örneğin, "master") arasındaki farkı gösteren bir form görünecektir.
4. Değişikliklerinizi ve MR ile ilgili detayları ekleyin.
5. MR oluştur düğmesine tıklayarak MR'yi oluşturun.

## Pull Request (PR) veya Merge Request (MR) Örneği

Aşağıda, bir Pull Request veya Merge Request örneği sunuyorum:

Diyelim ki bir ekip, bir web uygulamasında yeni bir özellik eklemek istiyor ve bu özelliği "feature-branch" adında yeni bir dal oluşturarak geliştiriyorlar. Ardından, bu özellikleri "master" ana dalına entegre etmek için bir PR veya MR oluşturuyorlar.

1. İlk adımda, ekip üyeleri "feature-branch" adlı daldaki kodlarını geliştirirler.

2. Daha sonra, bu değişiklikleri GitHub veya GitLab'a yüklerler (örneğin, `git push origin feature-branch`).

3. GitHub veya GitLab arayüzünde, "New Pull Request" (GitHub) veya "New Merge Request" (GitLab) düğmesine tıklarlar.

4. Karşılaştırmak istedikleri dallar arasındaki farkı görüntülerler. Yani, "feature-branch" ile "master" arasındaki farkı inceleyebilirler.

5. PR veya MR'ye başlık ve açıklama eklerler, yapılan değişiklikleri ve amaçlarını açıklarlar.

6. Diğer ekip üyeleri veya proje sahibi bu PR veya MR'yı inceleyip gerekirse geri bildirimde bulunurlar.

7. Sonunda, PR veya MR proje sahibi tarafından kabul edilirse, "Merge" düğmesine tıklanarak değişiklikler ana dala entegre edilir.

Bu, ekibin yeni özellikleri ana projeye başarıyla entegre etmek için Pull Request veya Merge Request kullanarak işbirliği yapmasının tipik bir örneğidir.

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

## Git Merge

- **Merge**: Git Merge, iki dalı birleştirir ve sonuçta birleştirme commit'i oluşturur. Bu, farklı dallardaki değişiklikleri birleştirmek için kullanılır.

- **Merge Kullanım**: 
  ```shell
  git merge [diğer dal]
  ```

  Örnek: `git merge feature-login` (feature-login dalını mevcut dal ile birleştirir)

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


