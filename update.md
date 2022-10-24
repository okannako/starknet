##### * Güncelleme için aşağıdaki adımları yapmak yeterli, en altta linki bulunan videoyla da işlemleri adım adım yapabilirsiniz. Bu işlemler ilk videomdan yapanlar için geçerlidir.
##### * İlk işlem olarak ``tmux ls`` yazıp tmux ekranlarını sıralıyoruz. Daha sonra starknet node çalıştığı tmux ekranına ```tmux attach -t ekranismi``` yazarak giriş yapıyoruz.
##### * Daha sonra ``ctrl+c`` ye basarak node durduruyoruz ve ``ctrl+b`` ye basıp daha sonra sadece ``d`` ye basarak tmuxdan çıkıyoruz. 
##### * Aşağıdaki kodları sırayla giriyoruz. Versiyon kısmına işlemleri yaptığınız zamanda en son hangi versiyon ise (https://github.com/eqlabs/pathfinder buradan bakınız) onu giriyoruz. Yeni bir tmux açmamızın nedeni işlemler uzun sürdüğü için Putty ile olan bağlantı kesilirse yükleme işleminde sorun olmasını engellemek. Son koddan sonra başlayan işlem uzun sürüyor.
```
cd
cd pathfinder
git pull
git checkout v0.3.1
tmux
cargo build --release --bin pathfinder
```
##### * Eğer yükleme sırasında rust versiyonu ile ilgili sorun çıkartırsa şu siteden https://www.rust-lang.org/tr/tools/install son versiyonu yükleyin.
##### * Yükleme bittikten sonra ``ctrl+b`` ye basıp daha sonra sadece ``d`` ye basarak tmuxdan çıkıyoruz. ``tmux ls`` yazıp açık olan tmux ekranlarından ilk başta çıktığımız ekrana geri dönüyoruz ve çalıştırma kodu olan aşağıdaki kod ile node tekrar başlatıyoruz. Burada https://mainnet.xxxxxxxxxxx devam eden link size özel Alchemy ya da Infura'dan aldığınız link. İlk videoda nasıl aldığınızı göstermiştim. Zaten eskisi hala geçerli yeni almanıza gerek yok.
```cargo run --release --bin pathfinder -- --ethereum.url https://mainnet.xxxxxxxxxxx```

##### * Bu koddan sonra node sorunsuz bir şekilde çalışmaya başlaması lazım eğer sorun çıkarıyorsa adımlarınızda bir hata vardır, tekrar kontrol edin.

##### * Kurulum Videosu
  * https://www.youtube.com/watch?v=xS5KkJSBj2I&t=1s
##### * Güncelleme Videosu
  * https://www.youtube.com/watch?v=0o4q-sNPxIA

##### * Hata alırsanız şu iki kodu node durdurduktan sonra venv için çalıştırın ve sonradan tekrar start yapın.
```
PIP_REQUIRE_VIRTUALENV=true pip install --upgrade pip
PIP_REQUIRE_VIRTUALENV=true pip install -r requirements-dev.txt
```
