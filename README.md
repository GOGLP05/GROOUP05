<!DOCTYPE html>
<html lang="ja">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>株式会社Jecコンサルティング</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha3/dist/css/bootstrap.min.css" rel="stylesheet">
  <style>
    /* カスタムスタイル */
    body {
      font-family: 'Arial', sans-serif;
      background-color: #f8f9fa;
      color: #333;
    }

    header {
      background: linear-gradient(90deg, #007bff, #6610f2);
      color: white;
      padding: 60px 0;
      text-align: center;
    }

    header h1 {
      font-size: 2.8rem;
      font-weight: bold;
    }

    header p {
      font-size: 1.2rem;
      margin-top: 10px;
    }

    .services-section {
      background-color: #fff;
      padding: 60px 20px;
    }

    .services-section h2 {
      text-align: center;
      font-weight: bold;
      margin-bottom: 40px;
    }

    .card:hover {
      transform: scale(1.05);
      transition: 0.3s ease-in-out;
    }

    .contact-section {
      background-color: #f1f1f1;
      padding: 60px 20px;
    }

    .contact-section h2 {
      text-align: center;
      font-weight: bold;
      margin-bottom: 40px;
    }

    footer {
      background-color: #343a40;
      color: white;
      text-align: center;
      padding: 20px 0;
      font-size: 0.9rem;
    }

    footer a {
      color: #0dcaf0;
      text-decoration: none;
    }

    footer a:hover {
      text-decoration: underline;
    }
  </style>
</head>

<body>
  <!-- ヘッダー -->
  <header>
    <h1>株式会社Jecコンサルティング</h1>
    <p>未来を切り拓くソリューションをご提供します。</p>
  </header>

  <!-- サービスセクション -->
  <section class="services-section">
    <div class="container">
      <h2>当社のサービス</h2>
      <div class="row text-center">
        <div class="col-md-4">
          <div class="card shadow-sm">
            <div class="card-body">
              <h5 class="card-title">経営コンサルティング</h5>
              <p class="card-text">お客様の事業を成功に導くための戦略的アプローチをご提供します。</p>
            </div>
          </div>
        </div>
        <div class="col-md-4">
          <div class="card shadow-sm">
            <div class="card-body">
              <h5 class="card-title">ITソリューション</h5>
              <p class="card-text">最新のテクノロジーを活用した効率的なITソリューションを提案します。</p>
            </div>
          </div>
        </div>
        <div class="col-md-4">
          <div class="card shadow-sm">
            <div class="card-body">
              <h5 class="card-title">市場調査</h5>
              <p class="card-text">正確な市場分析でお客様の意思決定をサポートします。</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- お問い合わせセクション -->
  <section class="contact-section">
    <div class="container">
      <h2>お問い合わせ</h2>

      <?php
      // フォームが送信されたときの処理
      if ($_SERVER["REQUEST_METHOD"] == "POST") {
        $name = htmlspecialchars($_POST["name"]);
        $email = htmlspecialchars($_POST["email"]);
        $message = htmlspecialchars($_POST["message"]);

        // メール送信設定
        $to = "your-email@example.com"; // 宛先メールアドレスを入力してください
        $subject = "【お問い合わせ】株式会社Jecコンサルティング";
        $body = "お名前: $name\nメールアドレス: $email\n\nメッセージ:\n$message";
        $headers = "From: $email";

        // メール送信処理
        if (mail($to, $subject, $body, $headers)) {
          echo '<div class="alert alert-success">お問い合わせを受け付けました。ありがとうございました。</div>';
        } else {
          echo '<div class="alert alert-danger">エラーが発生しました。もう一度お試しください。</div>';
        }
      }
      ?>

      <form method="POST" action="">
        <div class="mb-3">
          <label for="name" class="form-label">お名前</label>
          <input type="text" class="form-control" id="name" name="name" placeholder="お名前を入力してください" required>
        </div>
        <div class="mb-3">
          <label for="email" class="form-label">メールアドレス</label>
          <input type="email" class="form-control" id="email" name="email" placeholder="メールアドレスを入力してください" required>
        </div>
        <div class="mb-3">
          <label for="message" class="form-label">メッセージ</label>
          <textarea class="form-control" id="message" name="message" rows="5" placeholder="お問い合わせ内容を入力してください" required></textarea>
        </div>
        <button type="submit" class="btn btn-primary w-100">送信</button>
      </form>
    </div>
  </section>

  <!-- フッター -->
  <footer>
    <p>&copy; 2025 株式会社Jecコンサルティング. All Rights Reserved.</p>
    <p><a href="#">プライバシーポリシー</a> | <a href="#">利用規約</a></p>
  </footer>

  <!-- BootstrapのJS -->
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha3/dist/js/bootstrap.bundle.min.js"></script>
</body>

</html>
<!---->
