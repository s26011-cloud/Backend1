@RestController
public class LoginController {

    @PostMapping("/login")
    public String login(@RequestParam String id, @RequestParam String pw) {

        if(id.equals("admin") && pw.equals("1234")) {
            return "로그인 성공!";
        } else {
            return "로그인 실패!";
        }
    }
}