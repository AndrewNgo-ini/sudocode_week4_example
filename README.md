### Objective:
We are preparing the text file to work with **Word2Vec**, a model used to process and analyze text. By looking at the original file, we noticed that each sentence is separated by **three spaces**. To make it easier to handle later, we’ll split the text into sentences first.

The commands below will **clean** and **reformat** the large text file (`viwik18.txt`) by splitting the text wherever there are **three or more spaces**. This will create a new file (`clean_viwik18.txt`) where each sentence is on its own line.

The `head` command will let us check the first 10 lines of the new file to make sure everything worked properly.

You can download the cleaned file here: https://drive.google.com/file/d/15UaPnCrssA9GKvvEqQer2ouUUHKlRKYU/view?usp=sharing
---

### Command Breakdown:

1. **Command**:
   ```bash
   sed 's/   */\n/g' viwik18.txt > clean_viwik18.txt
   ```

   - **`sed`**: A tool used to edit text in a file.
   - **`'s/   */\n/g'`**: This part does the following:
     - **`s/.../.../g`**: Finds a pattern and replaces it. 
     - **`/   *`**: Finds three or more spaces in the text.
     - **`\n`**: Replaces the spaces with a **newline**, which moves the text to a new line.
     - **`g`**: This means the replacement happens throughout the file.
   - **`viwik18.txt`**: The input file we’re working with.
   - **`> clean_viwik18.txt`**: The output file where the changes will be saved. The new file will have each sentence on a new line.

2. **Command**:
   ```bash
   head -n 10 clean_viwik18.txt
   ```

   - **`head -n 10`**: This command shows the first 10 lines of the file.
   - **`clean_viwik18.txt`**: This is the file we just created. Using `head`, you can check that the sentences have been properly split into new lines.
   - Example:
```bash
head -n 10 clean_viwik18.txt
trang chính
internet society
internet society hay isoc là một tổ chức quốc tế hoạt động phi lợi nhuận phi chính phủ và bao gồm các thành viên có trình độ chuyên ngành tổ chức này chú trọng đến tiêu chuẩn giáo dục và các vấn đề về chính sách với trên một bốn năm tổ chức thành viên và sáu năm không không không thành viên cá nhân isoc bao gồm những con người cụ thể trong cộng đồng internet mọi chi tiết có thể tìm thấy tại website của isoc
internet society nằm ở gần thủ đô washington dc hoa kỳ và geneva thụy sĩ số hội viên của nó bao gồm hơn một bốn năm tổ chức thành viên và hơn sáu năm không không không cá nhân thành viên còn có thể tự lập một chi nhánh của tổ chức tùy theo vị trí hoặc sở thích hiện nay tổ chức có tới chín không chi nhánh trên toàn thế giới
nhiệm vụ và mục đích hoạt động
bảo đảm cổ vũ cho sự phát triển mở rộng và sử dụng internet được thuận lợi nhất cho mọi người trên toàn thế giới
xem thêm
lịch sử internet
liên kết ngoài
isoc việt nam
```
---
