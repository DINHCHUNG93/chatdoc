
xây dựng bộ não riêng cho doanh nghiệp: giải mã onyx - bá chủ mã nguồn mở.

đây là con hàng ôm hơn 20.000 stars trên GitHub, dư sức giúp ae tự tay dựng lên một hệ thống tri thức (knowledge base) đánh bật cả ChatGPT bản enterprise.

hệ thống này tự trang bị máy tìm kiếm lai (hybrid search) và mạng lưới tri thức (knowledge graph) siêu việt. đến mức nội bộ Netflix với 14.000 nhân sự cũng đang phải dựa lưng vào nó để dọn dẹp mớ rác dữ liệu phân mảnh tàn khốc của họ.

1. bài toán cốt lõi mà onyx đập tan
data công ty ae có đang rải rác khắp nơi không? tin nhắn trên Slack, file cất mốc trong Google Drive, rồi lại chắp vá thêm hàng tá ghi chú trên Notion. mỗi lần tìm một quy trình hay tài liệu là một lần mò kim đáy bể.
onyx sinh ra để kết liễu thảm họa này.

nó cắm sẵn hơn 50 cái connector (đầu nối) ăn liền. tự động hút data từ mọi nền tảng phổ thông về một mối. đỉnh cao nhất là nó kế thừa nguyên vẹn bộ phân quyền (permissions) có sẵn của doanh nghiệp.
đây không phải là một hệ thống RAG băm tài liệu ngớ ngẩn. nó tự build các liên kết chéo giữa các file để tạo ra một mạng lưới tri thức AI hoàn chỉnh. nó đọc hiểu bối cảnh sâu như một chuyên gia nghiên cứu thực thụ: chẻ nhỏ câu hỏi phức tạp ra và nhả lại đáp án cực kỳ sắc lẹm.

2. đưa vào thực chiến thế nào?
lõi công nghệ của con này cực kỳ tinh gọn: backend chạy Python, frontend dùng Next.js.
nó hỗ trợ Docker tận răng, ae chỉ việc ốp thẳng lên server là chạy mượt mà.

khi hệ thống đã lên luồng, ae chui vào màn hình quản trị và tha hồ nặn ra dàn trợ lý AI chuyên biệt cho từng phòng ban.
nó cân hết từ OpenAI đến Claude. muốn cắm VLLM để chạy model nội bộ (local)? vã được luôn.
đặc biệt, chỉ cần nắm được giao thức MCP, ae có thể nhồi thêm hàng tá vũ khí tự động hóa hạng nặng vào để con AI này trực tiếp thực thi công việc.

3. chốt chặn rủi ro bảo mật (tử huyệt phải nhớ)
một khi đã nạp toàn bộ tài liệu mật của công ty vào máy, thì bài toán phân quyền là mạng sống.

mặc dù onyx trang bị SSO và cô lập quyền đọc rất khét, nhưng dưới góc độ quản trị rủi ro, anh nhấn mạnh: phải bưng cái não lõi này nhét thẳng vào mạng nội bộ (intranet) có kiểm soát khép kín.
trong trường hợp kẹt phần cứng mà bắt buộc phải xài API của OpenAI để xử lý?
vào hệ thống khóa chết ngay cái giới hạn ngân sách (spending cap) lại. nạp hàng terabyte tài liệu vào mà thả rông luồng API thì tiền núi cũng cháy sạch trong một đêm.

ae nào đang đi tìm một kho chứa data bảo mật tại gia, hoặc muốn tự tay tối ưu lại hệ thống vận hành, thì bưng ngay con này về mổ xẻ.
link bốc hàng tận gốc cho ae mổ xẻ và ốp vào hệ thống:

• trang chủ: https://onyx.app/
• mã nguồn github: https://github.com/onyx-dot-app/onyx

cách đưa vào thực chiến? cực kỳ đơn giản. mở terminal lên và phang thẳng chuỗi lệnh này vào:

bước 1: kéo toàn bộ mã nguồn về máy.
git clone https://github.com/onyx-dot-app/onyx.git

bước 2: chui vào đúng thư mục và kích hoạt luồng hệ thống qua docker.
cd onyx/deployment/docker_compose
docker compose -p onyx-stack up -d

xong xuôi. hệ thống sẽ tự động build và chạy ngầm. ae chỉ việc truy cập vào giao diện và bắt đầu nhào nặn não bộ cho doanh nghiệp.

#vinmediaglobal #onyx #AI #rag #automation #knowledgemanagement #digitalmarketing


<!-- DANSWER_METADATA={"link": "https://github.com/danswer-ai/danswer/blob/main/README.md"} -->

<h2 align="center">
<a href="https://www.danswer.ai/"> <img width="50%" src="https://github.com/danswer-owners/danswer/blob/1fabd9372d66cd54238847197c33f091a724803b/DanswerWithName.png?raw=true)" /></a>
</h2>

<p align="center">
<p align="center">Open Source Gen-AI Chat + Unified Search.</p>

<p align="center">
<a href="https://docs.danswer.dev/" target="_blank">
    <img src="https://img.shields.io/badge/docs-view-blue" alt="Documentation">
</a>
<a href="https://join.slack.com/t/danswer/shared_invite/zt-2afut44lv-Rw3kSWu6_OmdAXRpCv80DQ" target="_blank">
    <img src="https://img.shields.io/badge/slack-join-blue.svg?logo=slack" alt="Slack">
</a>
<a href="https://discord.gg/TDJ59cGV2X" target="_blank">
    <img src="https://img.shields.io/badge/discord-join-blue.svg?logo=discord&logoColor=white" alt="Discord">
</a>
<a href="https://github.com/danswer-ai/danswer/blob/main/README.md" target="_blank">
    <img src="https://img.shields.io/static/v1?label=license&message=MIT&color=blue" alt="License">
</a>
</p>

<strong>[Danswer](https://www.danswer.ai/)</strong> is the AI Assistant connected to your company's docs, apps, and people. 
Danswer provides a Chat interface and plugs into any LLM of your choice. Danswer can be deployed anywhere and for any 
scale - on a laptop, on-premise, or to cloud. Since you own the deployment, your user data and chats are fully in your 
own control. Danswer is MIT licensed and designed to be modular and easily extensible. The system also comes fully ready 
for production usage with user authentication, role management (admin/basic users), chat persistence, and a UI for 
configuring Personas (AI Assistants) and their Prompts.

Danswer also serves as a Unified Search across all common workplace tools such as Slack, Google Drive, Confluence, etc.
By combining LLMs and team specific knowledge, Danswer becomes a subject matter expert for the team. Imagine ChatGPT if
it had access to your team's unique knowledge! It enables questions such as "A customer wants feature X, is this already
supported?" or "Where's the pull request for feature Y?"

<h3>Usage</h3>

Danswer Web App:

https://github.com/danswer-ai/danswer/assets/32520769/563be14c-9304-47b5-bf0a-9049c2b6f410


Or, plug Danswer into your existing Slack workflows (more integrations to come 😁):

https://github.com/danswer-ai/danswer/assets/25087905/3e19739b-d178-4371-9a38-011430bdec1b


For more details on the Admin UI to manage connectors and users, check out our 
<strong><a href="https://www.youtube.com/watch?v=geNzY1nbCnU">Full Video Demo</a></strong>!

## Deployment

Danswer can easily be run locally (even on a laptop) or deployed on a virtual machine with a single
`docker compose` command. Checkout our [docs](https://docs.danswer.dev/quickstart) to learn more.

We also have built-in support for deployment on Kubernetes. Files for that can be found [here](https://github.com/danswer-ai/danswer/tree/main/deployment/kubernetes).


## 💃 Main Features 
* Chat UI with the ability to select documents to chat with.
* Create custom AI Assistants with different prompts and backing knowledge sets.
* Connect Danswer with LLM of your choice (self-host for a fully airgapped solution).
* Document Search + AI Answers for natural language queries.
* Connectors to all common workplace tools like Google Drive, Confluence, Slack, etc.
* Slack integration to get answers and search results directly in Slack.


## 🚧 Roadmap
* Chat/Prompt sharing with specific teammates and user groups.
* Multi-Model model support, chat with images, video etc.
* Choosing between LLMs and parameters during chat session.
* Tool calling and agent configurations options.
* Organizational understanding and ability to locate and suggest experts from your team.


## Other Noteable Benefits of Danswer
* User Authentication with document level access management.
* Best in class Hybrid Search across all sources (BM-25 + prefix aware embedding models).
* Admin Dashboard to configure connectors, document-sets, access, etc.
* Custom deep learning models + learn from user feedback.
* Easy deployment and ability to host Danswer anywhere of your choosing.


## 🔌 Connectors
Efficiently pulls the latest changes from:
  * Slack
  * GitHub
  * Google Drive
  * Confluence
  * Jira
  * Zendesk
  * Gmail
  * Notion
  * Gong
  * Slab
  * Linear
  * Productboard
  * Guru
  * Bookstack
  * Document360
  * Sharepoint
  * Hubspot
  * Local Files
  * Websites
  * And more ...

## 💡 Contributing
Looking to contribute? Please check out the [Contribution Guide](CONTRIBUTING.md) for more details.
