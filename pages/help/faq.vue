<template>
  <div class="container py-5">
    <h2 class="h2 text-primary text-center mb-5">Frequently Asked Questions</h2>
    <div class="row">
      <div class="col-md-6 mx-auto">
        <!-- Nav tabs -->
        <ul
          class="nav justify-content-center nav-tabs"
          id="myTab"
          role="tablist"
        >
          <li class="nav-item" role="presentation">
            <button
              class="nav-link active px-5"
              id="home-tab"
              data-bs-toggle="tab"
              data-bs-target="#home"
              type="button"
              role="tab"
              aria-controls="home"
              aria-selected="true"
            >
              General
            </button>
          </li>
          <li class="nav-item" role="presentation">
            <button
              class="nav-link px-5"
              id="profile-tab"
              data-bs-toggle="tab"
              data-bs-target="#profile"
              type="button"
              role="tab"
              aria-controls="profile"
              aria-selected="false"
            >
              Business
            </button>
          </li>
        </ul>

        <!-- Tab panes -->
        <div class="tab-content">
          <div
            class="tab-pane active py-4"
            id="home"
            role="tabpanel"
            aria-labelledby="home-tab"
          >
            <template v-for="(i, index) in faqs_general">
              <div :key="index">
                <p>
                  <a
                    class="btn w-100 font-weight-bold text-primary text-left"
                    data-bs-toggle="collapse"
                    :href="'#question-' + index"
                    role="button"
                    aria-expanded="false"
                    aria-controls="solutions"
                  >
                    {{ i.question }}
                  </a>
                </p>
                <div class="collapse" :id="'question-' + index">
                  <small>{{ i.answer }}</small>
                </div>
              </div>
            </template>
          </div>
          <div
            class="tab-pane py-4"
            id="profile"
            role="tabpanel"
            aria-labelledby="profile-tab"
          >
            <template v-for="(i, index) in faqs_business">
              <div :key="index">
                <p>
                  <a
                    class="btn w-100 font-weight-bold text-primary text-left"
                    data-bs-toggle="collapse"
                    :href="'#questions-' + index"
                    role="button"
                    aria-expanded="false"
                    aria-controls="solutions"
                  >
                    {{ i.question }}
                  </a>
                </p>
                <div class="collapse" :id="'questions-' + index">
                  <small>{{ i.answer }}</small>
                </div>
              </div>
            </template>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "",
  data() {
    return {
      faqs_business: [
        {
          question:
            "How does FeedxPay simplify cross-border transactions for businesses?",
          answer:
            "FeedxPay simplifies cross-border transactions for businesses by providing a streamlined payment process, eliminating hidden fees, and offering real-time exchange rates. Our platform ensures swift and secure international transfers, making it easy for businesses to manage their global payments efficiently.",
        },
        {
          question:
            "What are the benefits of opening a multi-currency account with FeedxPay?",
          answer:
            "Opening a multi-currency account with FeedxPay offers numerous benefits. It allows you to hold and manage multiple currencies in one place, enabling cost-effective international transactions and reducing currency conversion fees. With our multi-currency accounts, businesses can seamlessly transact across borders without the complexities of dealing with different currencies.",
        },
        {
          question:
            "How secure and reliable are online money transfers with FeedxPay?",
          answer:
            "Online money transfers with FeedxPay are highly secure and reliable. We employ cutting-edge encryption technology to safeguard your funds and protect your transactions from unauthorized access. Our platform is built with robust security measures, ensuring a safe and seamless experience for all your online financial activities.",
        },
        {
          question:
            "Why choose FeedxPay for fast and cost-effective international money transfers?",
          answer:
            "Choosing FeedxPay for fast and cost-effective international money transfers is a smart decision. We offer competitive exchange rates and low transfer fees, ensuring that you get the best value for your transactions. Our platform guarantees quick and secure delivery of funds, providing you with peace of mind when sending money globally.",
        },
        {
          question:
            "What currencies are supported in FeedxPay's multi-currency accounts?",
          answer:
            "FeedxPay's multi-currency accounts support various major currencies, including NGN, USD, EUR, GBP, JPY, AUD, and more. You can conveniently transact in these currencies, making it easy to conduct business and manage finances across different countries.",
        },
        {
          question:
            "How can businesses leverage FeedxPay's payment gateway for seamless transactions?",
          answer:
            "Businesses can leverage FeedxPay's payment gateway for seamless transactions by integrating our secure API into their systems. This integration allows them to process cross-border payments smoothly, automating the payment flow and enabling easy reconciliation of transactions.",
        },
        {
          question:
            "What innovative features does FeedxPay offer for personal finance management?",
          answer:
            "FeedxPay offers innovative features for personal finance management, empowering users to take control of their finances. Our platform provides budgeting tools, spending analysis, and transaction categorization, giving users valuable insights to make informed financial decisions.",
        },
        {
          question:
            "How does blockchain technology enhance security in FeedxPay's cross-border transactions?",
          answer:
            "Blockchain technology enhances security in FeedxPay's cross-border transactions by ensuring tamper-proof records and immutability. Each transaction is recorded on the blockchain, providing transparency and reducing the risk of fraud. This level of security instills trust and confidence in our users.",
        },
        {
          question:
            "What sets FeedxPay's digital wallets apart in the fintech market?",
          answer:
            "FeedxPay's digital wallets stand out in the fintech market due to their user-friendly interface, quick access to funds, and support for multiple currencies. Our digital wallets offer a seamless and convenient way to make transactions, whether it's for everyday purchases or cross-border payments.",
        },
        {
          question:
            "How can individuals and businesses optimize forex transactions with FeedxPay?",
          answer:
            "Individuals and businesses can optimize forex transactions with FeedxPay by accessing real-time exchange rates, employing smart hedging strategies, and utilizing our tools for intelligent currency conversion. These features enable users to make informed decisions and maximize the value of their foreign exchange transactions.",
        },
        {
          question:
            "What insurtech solutions are available to users of FeedxPay's fintech platform?",
          answer:
            "Users of FeedxPay's fintech platform can benefit from various insurtech solutions, including tailored insurance products and coverage options. These solutions provide users with financial security and protection, ensuring peace of mind during unexpected events.",
        },
        {
          question:
            "How can FeedxPay's mobile banking app simplify financial tasks on the go?",
          answer:
            "FeedxPay's mobile banking app simplifies financial tasks on the go by offering a user-friendly interface and a range of convenient features. With our app, users can manage accounts, make payments, and access personalized financial insights anytime and anywhere, making financial management effortless.",
        },
        {
          question:
            "Why is FeedxPay's peer-to-peer lending platform a smart choice for borrowers and investors?",
          answer:
            "FeedxPay's peer-to-peer lending platform is a smart choice for borrowers and investors due to its competitive interest rates, diverse investment opportunities, and efficient loan processing. Borrowers can access funds quickly, while investors can diversify their portfolios and potentially earn attractive returns.",
        },
        {
          question:
            "How does FeedxPay utilize open banking to empower users with financial data?",
          answer:
            "FeedxPay utilizes open banking to empower users with financial data from multiple accounts in one place. This integration allows users to have a comprehensive view of their finances, enabling better financial decisions and personalized recommendations.",
        },
        {
          question:
            "What are the benefits of using FeedxPay's robo-advisors for investment guidance?",
          answer:
            "Using FeedxPay's robo-advisors for investment guidance offers numerous benefits. Our robo-advisors provide automated portfolio management, data-driven insights, and access to diversified investment options, helping users make informed investment decisions to achieve their financial goals.",
        },
        {
          question:
            "How does FeedxPay ensure data privacy and security in its financial technology solutions?",
          answer:
            "FeedxPay ensures data privacy and security in its financial technology solutions through robust encryption, multi-factor authentication, and strict adherence to industry regulations. We prioritize the protection of user data and employ the latest security measures to safeguard their information.",
        },
        {
          question:
            "What sets FeedxPay's contactless payment options apart for convenient and secure transactions?",
          answer:
            "FeedxPay's contactless payment options stand apart for their convenience and security. With just a tap or wave, users can make quick and secure transactions, reducing the need for physical contact and ensuring a seamless payment experience.",
        },
        {
          question:
            "How does FeedxPay's AI technology enhance personalized financial insights for users?",
          answer:
            "FeedxPay's AI technology enhances personalized financial insights for users by analyzing their spending patterns, financial behaviors, and goals. This analysis enables us to offer tailored recommendations and insights that align with each user's unique financial situation.",
        },
        {
          question:
            "What steps does FeedxPay take to provide a smooth user experience in cross-border transactions?",
          answer:
            "FeedxPay takes several steps to provide a smooth user experience in cross-border transactions. We offer user-friendly interfaces, real-time tracking of transactions, and proactive customer support to address any queries or issues promptly.",
        },
        {
          question:
            "Why choose FeedxPay as your go-to Neo bank for multi-currency needs and international payments?",
          answer:
            "Choose FeedxPay as your go-to Neo bank for multi-currency needs and international payments because we offer a safe, quick, and reliable solution. Our platform ensures hassle-free global banking with competitive rates, robust security, and a commitment to simplifying banking for our valued users.",
        },
      ],
      faqs_general: [
        {
          question: "What is Feedxpay?",
          answer:
            "FeedxPay is an innovative Neo bank that offers digital banking services, providing seamless and secure cross-border payments and a range of other financial solutions.",
        },
        {
          question: "Is my money safe with Feedxpay?",
          answer:
            "Absolutely! FeedxPay prioritizes the security of your funds. We use advanced encryption and security measures to protect your money and personal information.",
        },
        {
          question: "How can I open an account with Feedxpay?",
          answer:
            "Opening an account with FeedxPay is easy and convenient. Simply visit our website, click on 'Sign Up', and follow the simple registration process.",
        },
        {
          question:
            "Are there any fees associated with opening or maintaining an account?",
          answer:
            "We believe in transparency. FeedxPay has no hidden fees. Our account setup and maintenance are fee-free, ensuring a straightforward banking experience.",
        },
        {
          question:
            "What security measures are in place to protect my account and personal information?",
          answer:
            "FeedxPay employs industry-leading security protocols, including two-factor authentication, to safeguard your account and personal data.",
        },
        {
          question: "Can I link my other bank accounts to my FeedxPay account?",
          answer:
            "Yes, you can link your other bank accounts to your FeedxPay account for easy fund transfers and a comprehensive financial overview.",
        },
        {
          question:
            "How long does it take to transfer money to and from my FeedxPay account?",
          answer:
            "Transfers to and from your FeedxPay account are fast and efficient. Most transactions are completed within one business day.",
        },
        {
          question: "Can I deposit cash or checks into my FeedxPay account?",
          answer:
            "As a digital neo bank, FeedxPay currently supports electronic transfers. We do not accept cash or check deposits at this time.",
        },
        {
          question: "Is there a minimum balance requirement for my account?",
          answer:
            "No, FeedxPay does not have any minimum balance requirements. You can maintain your account with any balance amount that suits you.",
        },
        {
          question:
            "Can I set up automatic bill payments with my FeedxPay account?",
          answer:
            "Yes, FeedxPay enables you to set up automatic bill payments, ensuring your bills are paid on time with minimal effort.",
        },
        {
          question: "Can I open joint accounts with other individuals?",
          answer:
            "Absolutely! FeedxPay allows you to open joint accounts, making it easy to manage shared finances with family or business partners.",
        },
        {
          question: "What is the process for closing my FeedxPay account?",
          answer:
            "Should you wish to close your account, simply contact our customer support, and they will guide you through the process.",
        },
        {
          question:
            "How long does it take to receive a response from customer support?",
          answer:
            "Our customer support team strives to provide prompt assistance. You can expect a response within one business day or sooner.",
        },
        {
          question:
            "Are there any rewards or cashback programs for using my FeedxPay account?",
          answer:
            "FeedxPay offers various rewards and cashback programs, allowing you to earn perks while using your account for transactions.",
        },
        {
          question:
            "Are there any limits on the number of transactions I can make per month?",
          answer:
            "FeedxPay provides generous transaction limits, ensuring you can conduct your financial activities without restrictions.",
        },
        {
          question:
            "Does FeedxPay offer investment or wealth management services?",
          answer:
            "Currently, FeedxPay focuses on digital banking and cross-border payments, but we are continuously expanding our services.",
        },
        {
          question:
            "Are there any limitations on the types of businesses I can pay using my FeedxPay account?",
          answer:
            "FeedxPay allows payments to a wide range of businesses, making it easy to settle transactions with various merchants.",
        },
        {
          question:
            "Does FeedxPay support mobile payments like Apple Pay or Google Pay?",
          answer:
            "Yes, FeedxPay is compatible with mobile payment platforms like Apple Pay and Google Pay for added convenience.",
        },
        {
          question:
            "What happens if I forget my account password or get locked out of my account?",
          answer:
            "If you forget your password or get locked out of your account, you can easily reset your password through the account recovery process.",
        },
        {
          question:
            "Are there any special offers or promotions for new customers?",
          answer:
            "Yes, FeedxPay often offers special promotions and rewards for new customers. Be sure to check our website or app for the latest offers.",
        },
      ],
    };
  },
};
</script>
<style>
.nav.nav-tabs li.nav-item .nav-link.active{
  border-top: 0;
  border-left: 0;
  border-right: 0;
  border-bottom: 2px solid green;
}
</style>
