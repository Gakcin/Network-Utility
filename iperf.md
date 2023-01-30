# İperf nedir ?
- Network üzerinde iki nokta arasında aktif ölçülebilir bant genişliğini test eden ve açık kaynak kodlu bir uygulamadır. https://iperf.fr/iperf-download.php#windows linkinden windows ve linux  kullanımı için olan versiyonları indirilebilir.
 #  iperf kullanımı
 - iPerf server-client modeliyle çalıştığı için Bir Pc server, diğer PC client olacak  şekilde  yapılandırma olması gerekir. ilgili .rar kurulum dosyaları sunucu ve istemci bilgisayarlarda  c:\dizini altına çıkartılır. 
 - Sunucunun yapılandırılması
   - Sonra sunucu bilgisayardan  "iperf3 -s" komutu çalıstırılır. Uygulama 5201 portunu kullanır. (şayet bir firewall varsa kurral yazılması gerekebilir.)
 - İstemcinin yapılandırılması
   - istemci bilgisayarda c:\ dizini altına  .rar  dosyası çıkartılır.
   - "iperf3 -c 172.16.20.64" => server olan cihazın IP adresi  yaılır ve komut  çalıştırılır.
   - Client tarafından server’a yapılan istek sayesinde sender ve receiver tarafta  Mbits/sec cinsinden bir bant genişliğine değeri sunar.
# Ek paremetreler
- iperf3 -c 172.16.20.64 -b 0m -i 2
 -b 0m -- sınırsız bant genişliği
-i 2      -- 2 saniyede bir ölçüm al

- iperf3 -c 172.16.20.64 -b 20m -i 2 -t 20
-t 20           -- 20 saniye boyunca test yap. Default da bu değer 10 saniyedir.