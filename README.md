<!DOCTYPE html>
<html>

<head>
    <meta charset="utf-8">
    <title>会員登録</title>
</head>

<body>


    <h1>会員登録フォーム</h1>
    <form action="" method="POST">
        <table>
            <tr>
                <td>メールアドレス</td>
                <td><input type="text" name="user_id"></td>
            </tr>
            <tr>
                <td>パスワード</td>
                <td><input type="password" name="password"></td>
            </tr>
            <tr>
                <td>性別</td>
                <td>男<input type="radio" name="sex1"></td>
                <td>女<input type="radio" name="sex1"></td>
            </tr>
            <tr>
                <td>生年月日</td>
                <td><input type="date" name="date"></td>
            </tr>
        </table>
        <input type="submit" value="登録">
    </form>
</body>

</html>
