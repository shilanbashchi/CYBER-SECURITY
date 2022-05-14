# CYBER-SECURITY
MY CYBER SECURITY LECTURES AND CODES 
# DDoS VE DoS ARASINDAKİ FARKLAR 
# DoS NEDİR?
DoS yani açılımıyla Denial Of Service  (Hizmet Reddi ) saldırgan makine/PC tarafından hedef sistemin çalışmasının aksatma amacı taşıyan saldırı türüdür .bu saldırı web trafiği engelleme ,bant genişliği düşürme şeklinde kendini gösterebilir .Bunlar en yaygın saldırı şekilleridir .Buradaki amaç makinayı ele geçirmek değil sistemin çalışmasını ve hizmet vermesini engellemektir .ilk DoS saldırısı 1974'te bir lise öğrencisi tarafından gerçekleştirilmiştir .
# DDoS NEDİR?
DDoS yani açılımıyla Distributed Denial Of Service (dağıtılmış Hizmet Reddi ) DoS' tan farkı DDoS 'un birden fazla saldırgan makina kullanarak saldırıyı gerçekleştirmesi bunun için zombi adı verilen ele geçirilen PC 'leri kullanarak botnetler ile hizmetleri aksatmasıdır .Buna bağlı olarakn DDoS un etki alanı daha fazla ve verdiği zarar daha yüksektir .DDoS ' un ilkn saldırısı 1999 yılında Minnesota Üniversitesine karşı Trinoo adlı araç ile gerçekleştirilmiştir .
# Dos ve DDos Saldırı Belirtileri

- Sistem hızının normale göre oldukça yavaşlaması ya da artık kullanılamaz hale gelmesi
- Normalin dışında sistem ağ trafiği olması
- Aşırı UDP, SYN ve GET/POST isteklerinin bulunması

# Dos ve DDos Türleri

- Volume Based DDoS (Hacim Odaklı Saldırılar): Sunucunun sahip olduğu bant genişliğinin üstünde istek paketleri gönderilmesidir.

- Protocol Based DDoS (Protokol Odaklı Saldırılar): OSI protokolünün 3.Katman (Network) ve 4.Katmanındaki (Transport) zafiyetin kullanılmasıyla gerçekleştirilir.

- Application Layer DDoS (Uygulama Katmanlı Saldırılar): OSI protokolünün 7.katmanı olan uygulama katmanında bulunan servislerin açıklarının kullanılmasıyla saldırı yapılır.

- HTTP Flood: Hedef sayfaya sürekli olarak get veya post istekleri gönderilerek sistemi zorlamaktır.

- UDP Flood: UDP protokolü kullanılarak saldırı gerçekleştirilir. Saldırgan tarafından bir bilgisayarın portlarına çok sayıda UDP paketi gönderilir. Saldırının hedefi olan bilgisayar portun kulanım durumunu kontrol eder kullanılmıyorsa ICMP paketi ile cevap verir. Çok sayıda UDP paketine karşılık çok sayıda ICMP paketi gönderilir. Sistem böylece erişilemez hale gelir.
- ICMP Flood: ICMP protokolü kurban sisteme ICMP istek paketleri yollar ve karşı sistemden cevap bekler. Bu şekilde çok sayıda isteğe karşılık cevap vermeye çalışan sistem zorlanır.

- Ping of Death: Büyük boyutlu ICMP istek paketinin hedef sisteme yollanarak hedef sistemin yorulmasıdır.

- Syn Flood: Tcp protokolü üçlü el sıkışma ile bağlantı gerçekleştirir. Bu üçlü el sıkışma işlemi, istemcinin sunucuya SYN mesajı göndererek bağlantı kurmak istediğini belirtir. Sunucu bu mesajı SYN-ACK mesajı göndererek kabul eder. Ardından istemci ACK yanıyla bağlantıyı gerçekleştirir. SYN flood saldırısı ise sunucunun beklediği ACK mesajını göndermez. İstekler sürekli artar ve sistem artık bağlantı kuramaz hale gelir.

- TearDrop: UDP protokolünde paketler parçalanarak bir sisteme gönderilir ve bu paketler ofsetlere bölünerek numaralandırılır. Ofset değerlerine göre tekrar birleştirilir. Bu ofset değerleri çakışmamalıdır.  Eğer çakışma durumu yaşanırsa sistemde işlem yapılamaması gibi durumlar ortaya çıkar. Teardrop saldırısında is bu ofsetler çakıştırılıp gönderilerek gerçekleştirilir.

- Smurf: Hedefe ping istek paketleri ağın directed broadcast adresine gönderilir paket bu şekilde ağdaki tüm cihazlara ping istek paketleri göndermiş olur. Ping istek paketlerinin dönüş adresleri değiştirilerek hedefin ip adresi yapılır. Ağdaki tüm cihazlar da hedef cihaza ping paketlerini yollar. Böylece saldırı hem gerçekleştirilirken hem de saldırganın kimliği saklanmış olur.

- DNS Poisoning: Dns alan adı ip eşleşmelerini sağlayarak kişinin web sitesine erişimini sağlayan sunuculardır. Saldırgan ulaşılmak istenen web sitesinin eşleşmesini bozarak başka bir ip adresine yönlendirerek buradaki hazırlamış olduğu zararlı içreklerle kurbana zarar verir. 

# Dos ve DDos Saldırı Engelleme Yöntemleri

Bu saldırıların gerçekleştirilmesi günümüzde oldukça basit olduğu için kurumlar ve sistemler için önemli bir tehdit unsurudur. Bu saldırıların özellikle DDos saldırısının tamamen engellenmesi için kesin bir yöntem bulunmamakla birlikte saldırıları hafifletmek için önlemler alınıp sistemin ağ altyapısının sağlam yapılandırılması gerekir. Saldırının engellemesinden önce saldırı öncesi önlemlerin alınması ve erken tespiti daha önemlidir.

- Güvenlik duvarı ve antivirüs yazılımı veya donanımı kullanılmalıdır.

- Sistem güncellemeleri zamanında yapılmalıdır.

- Ağ trafiği izlenilmelidir, olağandışı durumlar için ağ cihazları yapılandırılmalıdır. Yönlendiriciler için rate limiting özelliği, sahte ve bozuk paketlerin engellenmesi, SYN, ICMP ve UDP paketlerinin eşik değerlerinin belirlenmesi gibi yöntemler uygulanabilmektedir.

- Bant genişliği kurumun ihtiyacı olandan fazla olmalıdır.

- Büyük ölçekli kurumlar için İçerik Dağıtım Ağı (CDN) verilerin dünyada birden çok sunucuda saklanması- kullanımı uygulanabilir.


