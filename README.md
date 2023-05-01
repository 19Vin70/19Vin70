- 👋 Hi, I’m @19Vin70
- 👀 I’m interested in programming
- 🌱 I’m currently learning web development
- 📫 You can reach me at Gmail:
         alqasimquillo@gmail.com
         xiaoalqasim@gmail.com
         marvinsaik43@gmail.com
         
         
class App:
    def __init__(self):
        self.email_list = ['marvinsaik43@gmail.com', 'xiaoalqasim@gmail.com', 'alqasimquillo@gmail.com']
        self.name = "Marvin Quillo Saik"
        self.age = 24
        self.status = "Inlove with so many errors"

    def render(self):
        return f"""
            <div>
                <h1>My Information</h1>
                <p>Name: {self.name}</p>
                <p>Age: {self.age}</p>
                <p>Status: {self.status}</p>
                <MyInformation emails={self.email_list} />
            </div>
        """

class MyInformation:
    def __init__(self, emails):
        self.emails = emails

    def render(self):
        email_list_html = ""
        for email in self.emails:
            email_list_html += f"<li>{email}</li>"

        return f"""
            <div>
                <h2>Emails:</h2>
                <ul>{email_list_html}</ul>
            </div>
        """

app = App()
my_information = MyInformation(app.email_list)

print(app.render())
print(my_information.render())


<!---
19Vin70/19Vin70 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
