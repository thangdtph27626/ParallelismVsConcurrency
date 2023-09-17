# Phân biệt khái niệm xử lý Concurrency (đồng thời) và Parallelism (song song) 

Concurrency (đồng thời) đề cập đến khả năng chạy nhiều tính toán cùng một lúc, có thể được thực hiện bằng cách sử dụng một đơn vị xử lý duy nhất. Điều này đạt được thông qua các quy trình xen kẽ trên bộ xử lý trung tâm (CPU) hoặc chuyển đổi ngữ cảnh, giúp tăng lượng công việc hoàn thành cùng một lúc.

Mặt khác,  Parallelism (song song)  liên quan đến việc chạy nhiều tính toán đồng thời mà không thể thực hiện được bằng một đơn vị xử lý duy nhất. Tính song song yêu cầu nhiều bộ xử lý trung tâm (CPU) để tăng thông lượng và tốc độ tính toán của hệ thống. Hơn nữa, cách tiếp cận này sử dụng cách tiếp cận luồng điều khiển xác định với việc gỡ lỗi đơn giản hơn so với đồng thời.

Concurrency (đồng thời) đề cập đến việc thực hiện đồng thời nhiều tác vụ, trong khi Parallelism (song song) đề cập đến việc thực hiện nhiều thao tác cùng một lúc. Cả hai khái niệm đều đóng vai trò quan trọng trong việc thiết kế và tối ưu hóa hệ thống máy tính, vì vậy việc hiểu được sự khác biệt của chúng sẽ cho phép các nhà phát triển lựa chọn phương pháp phù hợp nhất cho ứng dụng của mình.

## So Sánh  Concurrency (đồng thời) và Parallelism (song song) 
<table class="has-fixed-layout">
    <thead>
        <tr>
            <th></th>
            <th>
                <font style="vertical-align: inherit;">
                    <font style="vertical-align: inherit;">Đồng thời</font>
                </font>
            </th>
            <th>
                <font style="vertical-align: inherit;">
                    <font style="vertical-align: inherit;">Sự song song</font>
                </font>
            </th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>
                <font style="vertical-align: inherit;">
                    <font style="vertical-align: inherit;">Sự định nghĩa</font>
                </font>
            </td>
            <td>
                <font style="vertical-align: inherit;">
                    <font style="vertical-align: inherit;">Chạy và quản lý nhiều tính toán cùng một lúc</font>
                </font>
            </td>
            <td>
                <font style="vertical-align: inherit;">
                    <font style="vertical-align: inherit;">Thực hiện đồng thời nhiều phép tính</font>
                </font>
            </td>
        </tr>
        <tr>
            <td>
                <font style="vertical-align: inherit;">
                    <font style="vertical-align: inherit;">Đạt được bởi</font>
                </font>
            </td>
            <td>
                <font style="vertical-align: inherit;">
                    <font style="vertical-align: inherit;">Các tiến trình xen kẽ trên một CPU</font>
                </font>
            </td>
            <td>
                <font style="vertical-align: inherit;">
                    <font style="vertical-align: inherit;">Nhiều CPU</font>
                </font>
            </td>
        </tr>
        <tr>
            <td>
                <font style="vertical-align: inherit;">
                    <font style="vertical-align: inherit;">Đơn vị xử lý</font>
                </font>
            </td>
            <td>
                <font style="vertical-align: inherit;">
                    <font style="vertical-align: inherit;">Có thể được thực hiện bằng cách sử dụng một đơn vị xử lý duy
                        nhất</font>
                </font>
            </td>
            <td>
                <font style="vertical-align: inherit;">
                    <font style="vertical-align: inherit;">Cần nhiều đơn vị xử lý</font>
                </font>
            </td>
        </tr>
        <tr>
            <td>
                <font style="vertical-align: inherit;">
                    <font style="vertical-align: inherit;">Cộng việc hoàn thành</font>
                </font>
            </td>
            <td>
                <font style="vertical-align: inherit;">
                    <font style="vertical-align: inherit;">Tăng năng suất bằng cách tăng công việc được thực hiện đồng
                        thời</font>
                </font>
            </td>
            <td>
                <font style="vertical-align: inherit;">
                    <font style="vertical-align: inherit;">Tăng cường thông lượng và tốc độ tính toán của hệ thống
                    </font>
                </font>
            </td>
        </tr>
        <tr>
            <td>
                <font style="vertical-align: inherit;">
                    <font style="vertical-align: inherit;">Tiếp cận</font>
                </font>
            </td>
            <td>
                <font style="vertical-align: inherit;">
                    <font style="vertical-align: inherit;">Phương pháp tiếp cận luồng điều khiển không xác định</font>
                </font>
            </td>
            <td>
                <font style="vertical-align: inherit;">
                    <font style="vertical-align: inherit;">Phương pháp tiếp cận luồng điều khiển xác định</font>
                </font>
            </td>
        </tr>
        <tr>
            <td>
                <font style="vertical-align: inherit;">
                    <font style="vertical-align: inherit;">Gỡ lỗi</font>
                </font>
            </td>
            <td>
                <font style="vertical-align: inherit;">
                    <font style="vertical-align: inherit;">Gỡ lỗi rất khó</font>
                </font>
            </td>
            <td>
                <font style="vertical-align: inherit;">
                    <font style="vertical-align: inherit;">Debug cũng khó nhưng đơn giản hơn so với concurrency</font>
                </font>
            </td>
        </tr>
    </tbody>
</table>


## Sự khác  biệt  Concurrency (đồng thời) và Parallelism (song song)  

Concurrency (đồng thời) và Parallelism (song song)  là hai khái niệm trong khoa học máy tính thường được gộp lại với nhau, tuy nhiên sự khác biệt của chúng có thể ảnh hưởng đến quyết định của bạn khi thiết kế hoặc tối ưu hóa hệ thống. Ở đây, chúng ta sẽ xem xét kỹ hơn từng khái niệm để làm nổi bật sự khác biệt của chúng.

 ### Phương pháp xử lý nhiều phép tính 

Concurrency (đồng thời) và Parallelism (song song)  là hai cách tiếp cận riêng biệt để xử lý nhiều phép tính. Sự khác biệt chính nằm ở cách họ quản lý và thực hiện nhiều nhiệm vụ cùng một lúc.

Concurrency (đồng thời) là khái niệm chạy và quản lý nhiều tính toán đồng thời trên CPU bằng cách xen kẽ các hoạt động của chúng. Nói cách khác, tính đồng thời đạt được thông qua chuyển đổi ngữ cảnh, trong đó CPU chuyển đổi qua lại giữa các quy trình khác nhau để tạo ảo giác rằng nhiều tác vụ đang chạy cùng một lúc.

Ngược lại, Parallelism (song song)  đề cập đến việc thực hiện nhiều phép tính đồng thời bằng nhiều CPU. Mỗi CPU được giao một nhiệm vụ riêng biệt và tất cả các hoạt động này diễn ra đồng thời, tạo ra khả năng thực thi song song thực sự của các nhiệm vụ.


### Số lượng đơn vị xử lý cần thiết 

Tính Concurrency (đồng thời) và Parallelism (song song)  khác nhau ở số lượng bộ xử lý cần thiết để thực thi nhiều tác vụ cùng một lúc.

Một đơn vị xử lý, chẳng hạn như CPU ​​lõi đơn, có thể đạt được khả năng xử lý đồng thời bằng cách xen kẽ các tiến trình trên chip. Điều này cho phép nó thực hiện đồng thời nhiều tác vụ chỉ với một CPU.

Mặt khác, tính song song yêu cầu nhiều đơn vị xử lý thực hiện nhiều tác vụ cùng một lúc. Nhiều CPU có thể được sử dụng đồng thời cho nhiều tác vụ khác nhau để đảm bảo thực hiện công việc song song thực sự.


### Phương pháp tiếp cận và gỡ lỗi luồng điều khiển 

Concurrency (đồng thời) và Parallelism (song song)  khác nhau ở cách tiếp cận luồng điều khiển và độ khó của các vấn đề gỡ lỗi.

Concurrency (đồng thời) dựa trên mô hình luồng điều khiển không xác định, khiến không thể dự đoán thứ tự thực hiện tác vụ. Điều này làm cho việc gỡ lỗi trở nên khó khăn hơn vì khó xác định chính xác thời điểm các tác vụ được thực thi.

Ngược lại, cách tiếp cận luồng điều khiển xác định nhấn mạnh  Parallelism (song song), cho phép bạn dự đoán trước các nhiệm vụ và đơn giản hóa việc gỡ lỗi vì bạn biết chính xác thứ tự các nhiệm vụ của mình sẽ thực thi.

Việc gỡ lỗi có thể là thách thức ở cả Concurrency (đồng thời) và Parallelism (song song), mặc dù nó có xu hướng đơn giản hơn trong song song do cách tiếp cận luồng điều khiển xác định của nó.

### Quản lý nguồn tài nguyên

Quản lý tài nguyên là một khía cạnh không thể thiếu của cả Concurrency (đồng thời) và Parallelism (song song). Concurrency (đồng thời), khi nhiều tác vụ đang chạy trên một bộ xử lý, yêu cầu quản lý tài nguyên hiệu quả để đảm bảo mỗi tác vụ nhận được phần tài nguyên hợp lý. Chuyển đổi ngữ cảnh cho phép CPU chuyển đổi nhanh chóng giữa các tác vụ khác nhau theo định kỳ, nhưng việc xử lý sai có thể dẫn đến tiêu tốn không cần thiết và giảm hiệu suất.

Mặt khác, Parallelism (song song) liên quan đến nhiều bộ xử lý hoặc lõi và mỗi lõi có thể xử lý đồng thời nhiệm vụ riêng của mình. Quản lý tài nguyên song song đơn giản hơn so với đồng thời vì mỗi lõi có thể hoạt động độc lập mà không cần chuyển đổi ngữ cảnh. Hơn nữa, tính song song giúp sử dụng tốt hơn các tài nguyên sẵn có, dẫn đến thời gian thực thi nhanh hơn và hiệu suất tổng thể được cải thiện.

### Mô hình lập trình

Concurrency (đồng thời) và Parallelism (song song) đòi hỏi các mô hình lập trình khác nhau để tạo ra kết quả mong muốn. Việc thực hiện nhiệm vụ đồng thời xảy ra theo kiểu không thể đoán trước, có nghĩa là không có sự xác định trước nào tồn tại liên quan đến thứ tự nhiệm vụ. Điều này có thể dẫn đến tình trạng chạy đua, trong đó sự thành công hay thất bại của chương trình phụ thuộc vào thời điểm hoàn thành nhiệm vụ.

Concurrency (đồng thời) yêu cầu các mô hình lập trình sử dụng khóa, ngữ nghĩa hoặc các cơ chế đồng bộ hóa khác để phối hợp thực hiện tác vụ. Thật không may, điều này làm cho mã phức tạp hơn và khó gỡ lỗi hơn.

Parallelism (song song) cho phép các tác vụ được thực hiện theo kiểu có thứ tự, loại bỏ nhu cầu về cơ chế đồng bộ hóa để phối hợp thực hiện tác vụ. Điều này giúp đơn giản hóa các mô hình lập trình vì không cần cơ chế đồng bộ hóa để đảm bảo tính nhất quán của nhiệm vụ.

Hơn nữa, các mô hình lập trình song song có thể tận dụng tính song song vốn có trong một miền vấn đề, dẫn đến mã đơn giản hơn và hiệu quả hơn. Tuy nhiên, tính song song có thể tạo ra những thách thức mới như cân bằng tải và giao tiếp giữa các lõi.

### Độ chi tiết 

Concurrency (đồng thời) và Parallelism (song song) khác nhau về mức độ chi tiết. Mức độ chi tiết đề cập đến kích thước và độ phức tạp của các tác vụ hoặc luồng được thực thi, trong đó mỗi tác vụ hoặc luồng thực hiện một đơn vị nhỏ trước khi chuyển sang tác vụ hoặc luồng khác. Mặc dù điều này mang lại khả năng kiểm soát tinh chỉnh đối với việc thực hiện chương trình, nhưng nó cũng có thể dẫn đến chi phí cao hơn do chuyển đổi ngữ cảnh thường xuyên, làm giảm hiệu suất tổng thể.

Mặt khác,  Parallelism (song song) thường liên quan đến các nhiệm vụ hoặc luồng lớn hơn và phức tạp hơn được thiết kế để cộng tác trên một vấn đề hoặc nhiệm vụ chung. Mặc dù điều này có thể dẫn đến việc sử dụng tài nguyên xử lý tốt hơn và hiệu suất cao hơn nhưng nó cũng có thể gây ra nhiều thách thức hơn trong việc quản lý và gỡ lỗi. Mức độ chi tiết cần thiết phụ thuộc vào cả yêu cầu của chương trình cũng như tài nguyên phần cứng sẵn có.

###  7 sự thật cần biết 

- Đồng thời đề cập đến việc quản lý và thực hiện nhiều phép tính cùng một lúc, trong khi tính song song đề cập đến việc chạy nhiều phép tính cùng một lúc.
- Tính đồng thời đạt được bằng cách xen kẽ các quy trình trên bộ xử lý trung tâm (CPU) hoặc chuyển đổi ngữ cảnh; song song phụ thuộc vào nhiều CPU.
- Gỡ lỗi đồng thời là một vấn đề đặc biệt khó khăn, trong khi song song cũng có những khó khăn tương tự nhưng giải quyết đơn giản hơn.
- Tính đồng thời có thể đạt được chỉ bằng một đơn vị xử lý, trong khi tính song song yêu cầu nhiều bộ xử lý.
- Tính đồng thời cho phép hoàn thành nhiều công việc hơn cùng một lúc, trong khi tính song song giúp tăng thông lượng và tốc độ tính toán của hệ thống.
- Tính song song thực hiện đồng thời nhiều tác vụ, trong khi tính đồng thời liên quan đến việc xử lý nhiều tác vụ cùng một lúc.
- Đồng thời là một cách tiếp cận luồng điều khiển không xác định, trong khi song song có tính chất xác định.

### 8:Concurrency (đồng thời) và Parallelism (song song) cái nào tốt hơn? 

Phụ thuộc vào nhiệm vụ hiện tại và nguồn lực sẵn có. Có thể đạt được khả năng đồng thời chỉ với một CPU, khiến nó trở nên lý tưởng cho các tình huống có nhiều tác vụ liên quan đến I/O được hưởng lợi từ việc xen kẽ, chẳng hạn như máy chủ web. Tính song song yêu cầu nhiều CPU và hiệu quả hơn khi xử lý các tác vụ tính toán chuyên sâu có thể được chia thành các tác vụ phụ nhỏ hơn.
