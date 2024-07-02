30 Haziran 2024 itibarıyla CentOS 7, Destek Sonu (EOL) durumuna gelmiştir.

"Updated Repo as of 02.07.2024"

Bu, tüm CentOS 7 depolarının devre dışı bırakılacağı ve vault.centos.org'a taşınacağı anlamına geliyor.

Resmi destek sona ermiş olsa da, bazı kullanıcılar (öncelikle ticari olmayan kullanıcılar) bu arşivlenmiş depoları kullanarak yum ile paketleri kurmak isteyebilirler.

**UYARI:** Vault'ta bulunan paketlerin varlığı, güvenli oldukları anlamına gelmez. Vault, bu paketlerin son hallerinin bir arşividir. Bu paketleri üretim ortamlarında kullanmayın.

Bu depoları etkinleştirmek için aşağıdaki komutu çalıştırın:

```bash
sudo curl https://raw.githubusercontent.com/sdhmh/enable-centos-7-repo/main/CentOS-Base.repo --output /etc/yum.repos.d/CentOS-Base.repo
```

Bu komut, belirtilen URL'den `CentOS-Base.repo` dosyasını indirir ve `/etc/yum.repos.d/` dizinine kaydeder, böylece sisteminizin depo yapılandırmasını vault depolarını kullanacak şekilde günceller.
