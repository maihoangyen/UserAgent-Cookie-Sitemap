 # <div align="center"><p> UserAgent, Cookie, Sitemap </p></div>
 ## Họ và tên: Mai Thị Hoàng Yến
 ## Ngày báo cáo: Ngày 7/5/2022
 ### MỤC LỤC
 1. [User agent](#1)
 
     1.1 [User agent là gì?](#11)
      
     1.2 [User agent sử dụng trong HTTP](#12)
     
 2. [website để kiểm tra UA](#2) 
       
 3. [Tìm kiếm, cài đặt, chụp ảnh thực tế một vài Extension/Addon dùng để thay đổi UA trên Chrome và Firefox](#3)

     3.1 [Trên Chrome](#31)
      
     3.2 [Trên Firefox](#32)
     
 4. [Tìm hiểu về sitemap](#4)

     4.1 [sitemap là gì?](#41)
      
     4.2 [Các loại sitemap](#42)

     4.3 [Tại sao phải cần dùng sitemap](#43)
  
 5. [Tạo sitemap trên web cá nhân của mình](#5)

 6. [Tìm hiểu về Cookie](#6)

     6.1 [Cookie là gì?](#61)
      
     6.2 [Các loại cookie](#62)

     6.3 [ Lợi ích của Cookie](#63)

     6.4 [Rủi ro của Cookie](#64)
      
     6.5 [Chúng ta cần làm gì để sử dụng cookie an toàn](#65)

 7. [Tìm kiếm, cài đặt, chụp ảnh thực tế một vài Extension/Addon dùng để xem và thay đổi Cookie ](#7)

     7.1 [Trên Chrome](#71)
      
     7.2 [Trên Firefox](#72)

### Nội dung báo cáo 
#### 1. User agent <a name="1"></a>
<br> 1.1 User agent là gì? <a name="11"></a></br>
  - User agent thì nó là một chuỗi nhận dạng của trình duyệt khi gửi yêu cầu đến Web Server (máy chủ web). Khi trình duyệt web của bạn truy cập 1 trang Web bất kỳ, trình duyệt web của bạn có thể gửi một HTTP Request bao gồm chuỗi UA đến Web Server. Nội dung của UA tùy thuộc vào trình duyệt web các bạn dùng, mỗi trình duyệt đều có riêng 1 chuỗi UA nhất định. 
  
<br> 1.2 User agent sử dụng trong HTTP <a name="12"></a></br>
 - chuỗi User-Agent thường được sử dụng để thương lượng nội dung , trong đó máy chủ gốc chọn nội dung hoặc thông số hoạt động phù hợp cho phản hồi. Như với nhiều tiêu đề yêu cầu HTTP khác, thông tin trong chuỗi " User-Agent " góp phần vào thông tin mà máy khách gửi đến máy chủ, vì chuỗi này có thể khác nhau đáng kể từ người dùng này sang người dùng khác.
   - Định dạng cho các trình duyệt web do con người vận hành:
     - Định dạng của chuỗi User-Agent trong HTTP là danh sách các mã thông báo sản phẩm (từ khóa) với các nhận xét tùy chọn.  Ví dụ: nếu sản phẩm của người dùng được gọi là WikiBrowser, thì chuỗi User-Agent của họ có thể là WikiBrowser / 1.0 Gecko / 1.0 . Thành phần sản phẩm "quan trọng nhất" được liệt kê đầu tiên. Các phần của chuỗi này như sau:

       ` Tên và phiên bản sản phẩm ( WikiBrowser / 1.0 )`
       
       ` Công cụ bố trí và phiên bản ( Gecko / 1.0 )`
       
   - Định dạng cho tác nhân tự động (bot):
     - Các công cụ thu thập thông tin web tự động có thể sử dụng biểu mẫu đơn giản hóa, trong đó trường quan trọng là thông tin liên hệ trong trường hợp có sự cố. Theo quy ước từ "bot" được bao gồm trong tên của agent. Ví dụ:
     
       `Googlebot / 2.1 (+ http: //www.google.com/bot.html)`
     
   - User agent spoofing:
   
     - Các trang web thường bao gồm mã để phát hiện phiên bản trình duyệt để điều chỉnh thiết kế trang được gửi theo chuỗi tác nhân người dùng nhận được. Điều này có thể có nghĩa là các trình duyệt ít phổ biến hơn không được gửi nội dung phức tạp (mặc dù chúng có thể xử lý nó một cách chính xác) hoặc trong những trường hợp nghiêm trọng đã từ chối tất cả nội dung. Do đó, các trình duyệt khác nhau có tính năng che giấu hoặc giả mạo nhận dạng của chúng để buộc nội dung phía máy chủ nhất định. Ví dụ: trình duyệt Android tự nhận mình là Safari để hỗ trợ khả năng tương thích.
     - Các chương trình khách HTTP khác, như trình quản lý tải xuống và trình duyệt ngoại tuyến , thường có khả năng thay đổi chuỗi tác nhân người dùng.
     - Kết quả của việc giả mạo tác nhân người dùng có thể là số liệu thống kê được thu thập về việc sử dụng trình duyệt Web không chính xác.
     
   - User agent sniffing:
     - User agent sniffing là việc các trang web hiển thị nội dung khác nhau hoặc được điều chỉnh khi được xem với một số tác nhân người dùng nhất định.
     - User agent sniffing  được coi là hành vi kém, vì nó khuyến khích thiết kế dành riêng cho trình duyệt và phạt các trình duyệt mới có nhận dạng tác nhân người dùng không được công nhận. 
     - Chúng ta nên tạo đánh dấu HTML tiêu chuẩn, ho phép hiển thị chính xác trong nhiều trình duyệt nhất có thể và để kiểm tra các tính năng của trình duyệt cụ thể hơn là các phiên bản hoặc nhãn hiệu trình duyệt cụ thể.
     
   - Ký hiệu độ mạnh mã hóa:
     -  Trước đây đã sử dụng các chữ cái U, I và N để chỉ định độ mạnh mã hóa trong chuỗi tác nhân người dùng. "U" là viết tắt của "USA" (dành cho phiên bản có mã hóa 128 bit), "I" là viết tắt của "International" - trình duyệt có mã hóa 40 bit và có thể được sử dụng ở mọi nơi trên thế giới - và "N" là viết tắt của ( de facto ) cho "None" (không mã hóa). 
     -  Bây giờ, hầu hết các nhà cung cấp đều hỗ trợ mã hóa 256-bit.

   - Ngừng sử dụng tiêu đề User agent:
     - Google tuyên bố rằng một tính năng mới có tên là Client Hints sẽ thay thế chức năng của chuỗi User-Agent.

#### 2. website để kiểm tra UA <a name="2"></a>
 - Một số link website để kiểm tra UA:
   - https://www.whatsmyua.info
   - https://webbrowsertools.com/useragent/  
   - https://whatmyuseragent.com
   - https://dnschecker.org/user-agent-info.php
   - https://www.whatismybrowser.com
   
#### 3. Tìm kiếm, cài đặt, chụp ảnh thực tế một vài Extension/Addon dùng để thay đổi UA trên Chrome và Firefox <a name="3"></a>
 <br> 3.1 Trên Chrome <a name="31"></a></br>
   - Đầu tiên chúng ta sẽ vào google và gõ tìm kiếm `user agent switcher and manager chrome` kết quả hiện thị như bên dưới:

     ![image](https://user-images.githubusercontent.com/101852647/167112431-5c61d2bf-4f36-46aa-9352-d774496f1680.png)
   
   - Sau đó chúng ta nhấn vào và bắt đầu tải Extension cho chrome . Chúng ta sẽ nhấn `add to chrome`.

     ![image](https://user-images.githubusercontent.com/101852647/167112651-a86adcec-475c-4fe4-a5b4-d071cfc3134c.png)

   - Tiếp theo ta sẽ nhấn `add Extension` và bắt đầu đợi cài đặt.

     ![image](https://user-images.githubusercontent.com/101852647/167112747-8aafedfd-2b5f-488d-8a8c-fa9041bb77e2.png)

   - Sau khi cài đặt xong chúng ta sẽ được giao diện như hình bên dưới:

     ![image](https://user-images.githubusercontent.com/101852647/167113155-be4d0478-065c-455b-91ae-0fb30e7a69ea.png)

   - Đầu tiên để kiểm tra thử UA của chúng ta thì nhấn vào Test UA nó sẽ hiện thị UA của chúng ta :

     ![image](https://user-images.githubusercontent.com/101852647/167113442-7e0924fb-a8ae-4229-a34b-54d06425c253.png)
     
   - Giả sử để thay đổi UA chúng ta sẽ chọn trình duyệt trình duyệt Firefox và chọn hệ điều hành là linux chẳng hạn.

     ![image](https://user-images.githubusercontent.com/101852647/167113815-6bb3e3df-502d-4b61-ae49-c41a7d223e47.png)
     
     ![image](https://user-images.githubusercontent.com/101852647/167113852-2df60ebd-f9c0-43fa-8aad-285d5faa26bc.png)
     
   - Chúng ta có thể chọn bất cứ UA nào . Ở đây , mình chọn UA thứ 4. Sau đó nhấn `Apply (active window).

     ![image](https://user-images.githubusercontent.com/101852647/167114071-f2ed84d3-248c-4ecb-a6e9-4291e65cdcc1.png)

   - Sau đó chúng ta nhấn vào Test UA để kiểm tra xem UA đã thay đổi chưa. Chúng ta có thể thấy nó đã thay đổi UA so với lúc đầu.

     ![image](https://user-images.githubusercontent.com/101852647/167114453-d0c575fa-099e-46e2-8bd8-1595626d9a51.png)

  - Nếu chúng ta muốn thay đổi về lại UA ban đầu thì có thể nhấn Reset. Nó sẽ trả về UA ban đầu cho chúng ta.

    ![image](https://user-images.githubusercontent.com/101852647/167114687-6482a3e2-0057-4d79-a187-ca5f19945408.png)

<br> 3.2 Trên Firefox <a name="32"></a></br>

   - Đầu tiên chúng ta sẽ vào google và gõ tìm kiếm `user agent switcher and manager Firefox` kết quả hiện thị như bên dưới:

     ![image](https://user-images.githubusercontent.com/101852647/167116202-8b8098f1-c496-4a37-9a30-7307de428c99.png)
   
   - Sau đó chúng ta nhấn vào và bắt đầu tải Extension cho firefox . Chúng ta sẽ nhấn `Thêm vào firefox`.

     ![image](https://user-images.githubusercontent.com/101852647/167116281-74201de5-5bcc-4596-ab70-5507729e122c.png)

   - Tiếp theo ta sẽ nhấn `add` và bắt đầu đợi cài đặt.

     ![image](https://user-images.githubusercontent.com/101852647/167116312-b428a852-a289-41cc-9764-756659eb4178.png)

   - Sau khi cài đặt xong chúng ta sẽ được giao diện như hình bên dưới:

     ![image](https://user-images.githubusercontent.com/101852647/167116337-cf965734-84d4-4a58-8785-885b85d4d6ad.png)

   - Đầu tiên để kiểm tra thử UA của chúng ta thì nhấn vào Test UA nó sẽ hiện thị UA của chúng ta :

     ![image](https://user-images.githubusercontent.com/101852647/167116409-f34fa7bc-9575-4fe0-8e7a-8310fd58b23b.png)
     
   - Giả sử để thay đổi UA chúng ta sẽ chọn trình duyệt trình duyệt Chrome và chọn hệ điều hành là linux chẳng hạn.

     ![image](https://user-images.githubusercontent.com/101852647/167116475-a466a612-f164-4bde-a82f-fdef05a66d55.png)
     
     ![image](https://user-images.githubusercontent.com/101852647/167116500-07c3d47a-8255-4099-9178-0f039cd09084.png)
     
   - Chúng ta có thể chọn bất cứ UA nào . Ở đây , mình chọn UA thứ 3. Sau đó nhấn `Apply (active window).

     ![image](https://user-images.githubusercontent.com/101852647/167116850-d59f3e2c-6408-449c-b3f0-265da214bc9c.png)

   - Sau đó chúng ta nhấn vào Test UA để kiểm tra xem UA đã thay đổi chưa. Chúng ta có thể thấy nó đã thay đổi UA so với lúc đầu.

     ![image](https://user-images.githubusercontent.com/101852647/167116653-f3742951-2a32-4284-844f-d94091b1feac.png)

  - Nếu chúng ta muốn thay đổi về lại UA ban đầu thì có thể nhấn Reset. Nó sẽ trả về UA ban đầu cho chúng ta.

    ![image](https://user-images.githubusercontent.com/101852647/167116683-725b86b6-89a8-44fa-9270-1f73faca245f.png)

#### 4. Tìm hiểu về sitemap <a name="4"></a>
<br> 4.1 sitemap là gì? <a name="41"></a></br>
 - Sitemap (sơ đồ website) là một file liệt kê các trang và tệp tin trên website. Danh sách liệt kê được sắp xếp theo dạng sơ đồ phân tầng (giảm dần sự quan trọng) giúp các công cụ tìm kiếm:

   - Thu thập dữ liệu trên trang web của bạn hiệu quả hơn
   - Biết những URL nào bạn muốn ưu tiên xuất hiện
   - Hiển thị kết quả trên trang tìm kiếm thông minh hơn
   
<br> 4.2 Các loại sitemap <a name="42"></a></br>
 - Về mặt cấu trúc: 
   - Có 2 loại sitemap là XML và HTML.

     - XML (Dành cho bot của công cụ tìm kiếm) 

     - HTML (Hiển thị cho người dùng dễ truy cập trên các giao diện trang web)
     
         <table align="center">
          <tr>
            <td align="center" ><b>Sitemap</b></td>
            <td align="center"><b>XML</b></td>
            <td align="center"><b>HTML</b></td>   
          </tr>
          <tr>
            <td ><b>Đặc điểm</b></td>
            <td ><br><b>- Chứa các metadata chung với URL của website</b></br>
                 <br><b>- Chứa các thông tin về thời gian cập nhật</b></br>
            </td>  
            <td ><br><b>- Cung cấp chuyển hướng rõ ràng cho người dùng</b></br>
                 <br><b>- Dựa vào tính thân thiện thúc đẩy thứ hạng của website</b></br>
            </td> 
          </tr>
          <tr>
            <td ><b>Giống nhau</b></td>
            <td colspan="2" align="center"><b>XML và HTML đều cho phép trang web dễ dàng crawl bởi search engines</b></td>   
          </tr>
          <tr>
            <td><b>Khác nhau</b></td>
            <td><b>Dùng được cho search engine </b></td>      
            <td><b>Viết cho người dùng website</b></td>      
          </tr>

        </table>
    
- Về dạng: 

   <table align="center">
      <tr>
        <td align="center" ><b>Tên</b></td>
         <td align="center"><b>Chức năng</b></td>
      </tr>
      <tr>
         <td ><b>Sitemap Index</b></td>
         <td ><b> Tập hợp các Sitemap được đính kèm và được dùng để đặt trong file robots.txt</b></td>  
      </tr>
      <tr>
         <td ><b>Sitemap-category.xml</b></td>
         <td ><b>Tập hợp cấu trúc của các danh mục trên website.</b></td>   
      </tr>
      <tr>
         <td><b>Sitemap-products.xml</b></td>
         <td><b>Sitemap dành cho các link chi tiết về các sản phẩm trên trang. </b></td>          
      </tr>
      <tr>
         <td ><b>Sitemap-articles.xml</b></td>
         <td ><b>Giúp Google tìm thấy nội dung trên các trang web được chấp thuận cho Google Tin tức..</b></td>   
      </tr>
      <tr>
         <td ><b>Sitemap-tags.xml</b></td>
         <td ><b>Sitemap dành cho các thẻ trên website</b></td>   
      </tr>
      <tr>
         <td ><b>Sitemap-video.xml</b></td>
         <td ><b>Sitemap dành riêng cho video trên các page, website. Được sử dụng đặc biệt để giúp Google hiểu nội dung video trên trang của bạn</b></td>   
      </tr>
      <tr>
         <td ><b>Sitemap-image.xml</b></td>
         <td ><b>Giúp Google tìm thấy tất cả các hình ảnh được lưu trữ trên trang web của bạn</b></td>   
      </tr>
   </table>
  
<br> 4.3 Tại sao phải cần dùng sitemap <a name="43"></a></br>
 - Chúng ta luôn muốn Google thu thập dữ liệu mọi trang và liên kết quan trọng trên website một cách nhanh chóng. Sitemap sẽ là bản đồ điều hướng, giúp các bot của google có thể dễ dàng và nhanh chóng thu thập được dữ liệu nội dung trên website của chúng ta.
 
 - Sitemap còn có thể chứa các siêu dữ liệu về mỗi URL, thông báo sẽ được gửi đến cho chúng ta khi nó mới được cập nhật. Toàn bộ công việc của Sitemap là hướng dẫn cho các bộ máy tìm kiếm thu thập thông tin của trang web một cách hiệu quả đồng thời cập nhật những thay đổi trên trang web của bạn.Chính lý do này thì thiết kế web chuẩn SEO bắt buộc phải có Sitemap để đảm bảo Google và các công cụ tìm kiếm có thể thu thập dữ liệu một cách nhanh nhất.
 
#### 5. Tạo sitemap trên web cá nhân của mình <a name="5"></a>
 - Truy cập vào website http://www.xml-sitemaps.com/
 
   ![image](https://user-images.githubusercontent.com/101852647/167170299-3d87db73-d6ff-482c-9983-01920865a2ae.png)
 
 - Đây là trang web chính của mình.Coppy link web.

   ![image](https://user-images.githubusercontent.com/101852647/167172340-2603d223-3a7e-4d89-bdf2-aaeec1f919ff.png)

 - Nhập URL và chọn Start
   
   ![image](https://user-images.githubusercontent.com/101852647/167170402-204f6afd-2a9c-464f-bcb8-2e23bc138eb8.png)

- Sau khi quá trình xử lý kết thúc -> chọn View Sitemap Details

   ![image](https://user-images.githubusercontent.com/101852647/167170522-cb64772e-4994-418e-8626-402f911d9f15.png)

- Download Sitemap

   ![image](https://user-images.githubusercontent.com/101852647/167170683-8995ab8e-465a-47ac-85a9-1655c88f5544.png)

- Upload file XML lên host tại thư mục của website và kiểm tra với URL `https://testsitemapphp.000webhostapp.com/sitemap.xml`

  ![image](https://user-images.githubusercontent.com/101852647/167171986-44a3f83f-8c4e-455c-95c9-7a4d1b0580c0.png)

#### 6. Tìm hiểu về cookie <a name="6"></a>
<br> 6.1 Cookie là gì? <a name="61"></a></br>
 - Cookie là một bộ nhắc nhỏ mà website lưu trữ ở trên máy tính của bạn có thể định danh cho bạn. Khi bạn truy cập và một trang web, website này sẽ đặt một cookie tại trên máy đó, thay cho việc liên tục hỏi bạn các thông tin như nhau, chương trình trên website có thể sao lưu thông tin vào một cookie mà khi cần thông tin sẽ đọc cookie. Nếu không có cookie bạn sẽ phải nhập lại thông tin của mình trên mỗi màn hình web. Thông tin duy nhất mà cookie lưu trữ là thông tin mà bản thân bạn chia sẻ với website tạo ra cookie. Một website không thể đọc cookie của một công ty khác trừ khi công ty kia cung cấp cho công ty đó chứa khóa giải thích ý nghĩa của cookie.
 
<br> 6.2 Các loại cookie <a name="62"></a></br>
 - `Session Cookie`: được lưu trong bộ nhớ của máy tính chỉ trong phiên duyệt web và sẽ tự động xóa khỏi máy tính khi trình duyệt đóng lại. Những cookie này thường được lưu trữ dưới dạng ID. Nó cho phép bạn nhanh chóng chuyển tới một trang mới mà không cần đăng nhập lại. Chúng được sử dụng rộng rãi ở những trang web thương mại.
 - `Persistent Cookie`:  được lưu trữ trên ổ cứng của máy tính và không bị xóa khi trình duyệt đóng lại. Những cookie này có thể thiết lập những sở thích của bạn đối với mỗi trang web cụ thể khi bạn quay lại, cho phép những ưu đãi sẽ được sử dụng trong những lần trình duyệt tiếp theo.
 - `Cookie của bên thứ ba`: Thông thường, thuộc tính miền của cookie sẽ khớp với miền được hiển thị trong thanh địa chỉ của trình duyệt web. Đây được gọi là cookie của bên thứ nhất . Tuy nhiên, cookie của bên thứ ba thuộc về miền khác với miền được hiển thị trên thanh địa chỉ. Cookie cho phép các công ty tiếp thị hoặc quảng cáo.
 
<br> 6.3 Lợi ích của Cookie <a name="63"></a></br>
 - Đối với doanh nghiệp:
   - Doanh nghiệp có thể biết được một số thồng tin về những người đang truy cập web của mình, biết được mức độ thường xuyên truy cập cũng như thời gian chi tiết truy cập.

   - Doanh nghiệp có thể biết được sự cảm nhận của bạn khi duyệt web đó. Lưu trữ thông tin cá nhân của khách hàng, những thông tin này sẽ giúp khách hàng khi vào trang web đó lần sau sẽ thuận tiện hơn.

   - Doanh nghiệp sẽ dùng cookie để điều chỉnh các quảng cáo của mình, cung cấp cho biết những quảng cáo nào được xem nhiều nhất từ đó đưa ra biện pháp điều chỉnh hoặc thiết kế phù hợp.
   
 - Đối với người dùng: 
   - Chúng làm cho web tiện lợi hơn, người dùng có thể truy cập vào web nhanh hơn không phải nhập lại các thông tin nhiều lần.
   
<br> 6.4 Rủi ro của Cookie <a name="64"></a></br>
 - Cookie ảnh hưởng tới sự riêng tư của người dùng. cũng như rò rỉ thông tin cá nhân. Cookie theo dõi người dùng đã ghé thăm những nơi nào và đã xem những gì trên web.
 -  Bản thân các cookie không thể dùng để phát tán virus, mã độc. Tuy nhiên nó có thể thu thập khá nhiều thông tin cá nhân của bạn nhất là những thông tin bạn cung cấp trên trang web như thông tin thẻ tín dụng… nên cookie có thể làm tăng nguy cơ mất thông tin đăng nhập nếu như người khác sử dụng máy tính của bạn, hoặc trường hợp máy tính của bạn bị xâm nhập, đánh cắp.
 
<br> 6.5 Chúng ta cần làm gì để sử dụng cookie an toàn <a name="65"></a></br>
 - Thiết lập tùy chọn cookie bằng cách sử dụng cài đặt chế độ bảo mật cho trình duyệt.
 - Xóa cookie định kỳ trên máy tính
 - `Session Cookie` được tự động xóa khi hoàn thành một giao dịch, bằng việc xóa cookie của bạn theo định kỳ sẽ làm giảm nguy cơ của việc lạm dụng thông tin vô tình hay cố ý lưu trữ trong cookie
 - Không cho phép cookie được lưu trữ thông tin đăng nhập
 - Giữ cho hệ thống trình duyệt của bạn được tự động update các bản vá lỗi, cập nhật phần mềm chống phần mềm giả mạo, chỉ truy cập vào những trang web đáng tin cậy
 - Nếu bạn muốn chia sẻ dữ liệu trực tuyến của bạn với ai đó, đặt thiết lập bảo mật
 - Thận trọng khi chia sẻ máy tính của bạn, nếu bạn lưu trữ thông tin sử dụng cookie (username, password..) các cá nhân sử dụng máy tính của bạn có thể sẽ truy cập vào tài khoản của bạn và thực hiện các giao dịch qua tên bạn
 - Nên sử dụng các tiện ích để xóa bỏ các cookie ra khỏi đĩa cứng như IEClean hay NSClean…
 
#### 7. Tìm kiếm, cài đặt, chụp ảnh thực tế một vài Extension/Addon dùng để xem và thay đổi Cookie <a name="7"></a> 
<br> 7.1 Trên chrome <a name="71"></a></br>
  - Một số tính năng chính của công cụ quản lý cookie EditThisCookie:
    - Xóa bất kì cookie nào.
    - Chỉnh sửa cookie.
    - Thêm các cookie mới.
    - Tìm kiếm cookie.
    - Bảo vệ cookie (với chế độ read-only).
    - Chặn cookie (thông qua việc lọc cookie).
    - Xuất cookie sang file JSON, Netscape (phù hợp với wget và curl), Perl.
    - Nhập cookie từ file JSON.
    - Giới hạn ngày hết hạn tối đa của bất kì cookie nào.
  - Đầu tiên chúng ta sẽ vào google và gõ tìm kiếm `editthiscookie for chrome` kết quả hiện thị như bên dưới:

     ![image](https://user-images.githubusercontent.com/101852647/167181128-72651cac-58a3-45f0-b29f-c4648596fc0f.png)
   
   - Sau đó chúng ta nhấn vào và bắt đầu tải Extension cho chrome . Chúng ta sẽ nhấn `add to chrome`.

     ![image](https://user-images.githubusercontent.com/101852647/167181178-ad62b658-fa1b-4c6c-902d-6b62fa35b7ec.png)

   - Tiếp theo ta sẽ nhấn `add Extension` và bắt đầu đợi cài đặt.

     ![image](https://user-images.githubusercontent.com/101852647/167181231-19d989a5-92ea-4d61-b45c-7ff06163ce75.png)

   - Sau khi cài đặt hoàn tất Để xem cookie cho một website, mở website đó trên trình duyệt, click chọn biểu tượng của tiện ích EditThisCookie, khi đó một cửa sổ sẽ hiển thị tất cả các cookie đang hoạt động trên website đó. chúng ta sẽ được giao diện như hình bên dưới:

     ![image](https://user-images.githubusercontent.com/101852647/167181341-3a9b7b80-81bf-4fd2-9893-8e1348adefe5.png) 

   -  Để chỉnh sửa cookie, chỉ cần nhấp chuột vào cookie cần chỉnh sửa và gõ thông tin vào các trường thông tin hiển thị. Ta thấy thời gian là `00:40:47` bây giờ ta sẽ thay đổi giá trị thời gian thành `00:50:47` hoặc có thể thay đổi value bằng cách thêm vào `1234` và nhấn tick xanh. Như vậy là chúng ta có thể thay đổi cookie rồi.

      ![image](https://user-images.githubusercontent.com/101852647/167189290-18dd77d0-2d35-49a3-a7a5-a65bfcb8481f.png)
     
      ![image](https://user-images.githubusercontent.com/101852647/167189995-0e21c704-40d0-4337-b481-163fa1cb913a.png)

<br> 7.2 Trên Firefox <a name="72"></a></br>
- Đầu tiên chúng ta sẽ vào google và gõ tìm kiếm `editthiscookie for firefox` kết quả hiện thị như bên dưới:

     ![image](https://user-images.githubusercontent.com/101852647/167192111-1d632074-a804-4e83-a823-90764b419efc.png)
   
   - Sau đó chúng ta nhấn vào và bắt đầu tải Extension cho firefox . Chúng ta sẽ nhấn `Thêm vào firefox`.

     ![image](https://user-images.githubusercontent.com/101852647/167192488-8f643255-ad89-41c0-9b3c-4bccd9476308.png)

   - Tiếp theo ta sẽ nhấn `add ` và bắt đầu đợi cài đặt.

     ![image](https://user-images.githubusercontent.com/101852647/167192559-15ac3331-223f-4e92-9a89-1ba11edf1fca.png)
     
   - Sau khi cài đặt hoàn tất Để xem cookie cho một website, mở website đó trên trình duyệt, click chọn biểu tượng của tiện ích EditThisCookie, khi đó một cửa sổ sẽ hiển thị tất cả các cookie đang hoạt động trên website đó. chúng ta sẽ được giao diện như hình bên dưới:

     ![image](https://user-images.githubusercontent.com/101852647/167192655-b67a9882-4353-435d-aad4-92eb740e61e6.png)

   -  Để chỉnh sửa cookie, chỉ cần nhấp chuột vào cookie cần chỉnh sửa và gõ thông tin vào các trường thông tin hiển thị. Ta thấy thời gian là `00:59:47` bây giờ ta sẽ thay đổi giá trị thời gian thành `00:30:47` hoặc có thể thay đổi value bằng cách thêm vào `1234` và nhấn tick xanh. Như vậy là chúng ta có thể thay đổi cookie rồi.

     ![image](https://user-images.githubusercontent.com/101852647/167192721-c315cec1-a4be-4a8a-ad0b-2652d222b3d6.png)
     
     ![image](https://user-images.githubusercontent.com/101852647/167192943-9788c425-f727-433d-9eca-367de3dfedd3.png)
