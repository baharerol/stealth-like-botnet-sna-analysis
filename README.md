# Stealth-like Botnet Trafiğinin Zamansal Ağ Analizi

Samsun Üniversitesi - Yazılım Mühendisliği  
Sosyal Ağ Analizi Dersi Dönem Projesi

## Proje Hakkında

Bu proje, CTU-13 botnet veri seti üzerinde sosyal ağ analizi yöntemleri uygulayarak stealth-benzeri botnet davranışlarının tespit edilip edilemeyeceğini araştırmaktadır. Çalışma kapsamında ağ trafiği yönlü ve ağırlıklı bir graf olarak modellenmiş; merkezilik analizi, topluluk tespiti, zamansal ağ analizi ve ağ dayanıklılığı analizleri gerçekleştirilmiştir.

## Araştırma Sorusu

Zamansal sosyal ağ analizi yöntemleri kullanılarak stealth-benzeri botnet davranışları ağ trafiği içerisinde tespit edilebilir mi?

## Veri Seti

Çalışmada **CTU-13 Botnet Dataset** kullanılmıştır.

- Kaynak: https://www.stratosphereips.org/datasets-ctu13
- Kullanılan dosya: `capture20110818.binetflow`
- Düğüm sayısı: 197.824
- Kenar sayısı: 258.027

**Önemli:** Veri seti boyutu nedeniyle repoya dahil edilmemiştir. Yukarıdaki linkten indirilip proje ana klasörüne yerleştirilmelidir.

## Kullanılan Kütüphaneler

- `pandas` - veri işleme
- `networkx` - graf yapısı ve ağ metrikleri
- `python-louvain` - topluluk tespiti
- `matplotlib`, `seaborn` - görselleştirme
- `numpy` - sayısal işlemler

## Kurulum:
pip install -r requirements.txt

## Çalıştırma

1. Veri setini indirip ana klasöre koyun
2. Notebook'u açın: `jupyter notebook 221118005_SNA_Project.ipynb`
3. Hücreleri sırayla çalıştırın

## Temel Bulgular

- Ağ ölçeksiz (scale-free) yapıda; düğümlerin büyük kısmı 1-2 bağlantıya sahipken birkaç düğüm çok yüksek dereceye sahip
- En kritik düğüm: `147.32.84.229` (en yüksek degree, betweenness ve PageRank)
- Louvain algoritması ile 26 topluluk tespit edildi (modülarite: 0.54)
- Botnet trafiği belirli zaman aralıklarında ani spike'lar göstermektedir (stealth davranışı)
- Ağ hedefli saldırılara karşı kırılgan, rastgele arızalara karşı dayanıklı

## Yazar

Bahar Erol

Danışman: Dr. Öğr. Üyesi Özgür Tonkal

## Lisans

Akademik kullanım. CTU-13 veri seti kendi lisans şartlarına tabidir.
