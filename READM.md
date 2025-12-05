![Gvqz53CWwAAWtFz](https://github.com/user-attachments/assets/c0fe3347-2f64-4d8a-97b5-de0e09436c36)

# Windows’ta WSL + Ubuntu Kurulumu

Kendi bilgisayarınızda (ör. gensyn, boundless vb.) node çalıştırmak için WSL üzerinde **Ubuntu 22.04** kurulum rehberi.

---

## 1- WSL Kurulumu:

PowerShell’i **Yönetici** olarak aç ve WSL’yi kur:

```powershell
wsl --install
```

* Yeniden başlat isterse bilgisayarı yeniden başlat.
* İlk açılışta Linux kullanıcı adı ve şifre oluştur.

---

## 2- Ubuntu 22.04 Yükleme:

* Microsoft Store’da **Ubuntu 22.04** ara → **Install**
* Uygulamayı aç ve kurulumun tamamlanmasını bekle
* İstendiğinde kullanıcı adı ve şifre oluştur

---

## 3- Root Yetkisine Geçiş:

Node kurulumlarında root yetkisi gerekebilir:

```bash
sudo -i
```

---

## 4- Güncelleme ve Gerekli Araçlar:

Ubuntu terminalinde paketleri güncelle ve gerekli araçları kur:

```bash
sudo apt update && sudo apt upgrade -y
```
```bash
sudo apt install -y curl iptables build-essential git wget lz4 jq make gcc nano \
automake autoconf tmux htop nvme-cli libgbm1 pkg-config libssl-dev libleveldb-dev \
tar clang bsdmainutils ncdu unzip ca-certificates
```

---

## Son:

Bu aşamadan sonra hedef node’un (ör. **Boundless**) resmi kurulum adımlarına geçebilirsiniz.
