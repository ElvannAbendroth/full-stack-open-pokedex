# 11.1 Warming up
Think about a hypothetical situation where we have an application being worked on by a team of about 6 people. The application is in active development and will be released soon.

Let us assume that the application is coded with some other language than JavaScript/TypeScript, e.g. in Python, Java, or Ruby. You can freely pick the language. This might even be a language you do not know much yourself.

Write a short text, say 200-300 words, where you answer or discuss some of the points below. You can check the length with https://wordcounter.net/. Save your answer to the file named exercise1.md in the root of the repository that you shall create in exercise 11.2.

**The points to discuss:**

- Some common steps in a CI setup include linting, testing, and building. What are the specific tools for taking care of these steps in the ecosystem of the language you picked? You can search for the answers by Google.
- What alternatives are there to set up the CI besides Jenkins and GitHub Actions? Again, you can ask Google!
- Would this setup be better in a self-hosted or a cloud-based environment? Why? What information would you need to make that decision?
Remember that there are no 'right' answers to the above!

---

CI/CD pipelines have become an integral part of the DevOps culture.  In my hypothetical scenario, I chose to use Python as the language used by my team of 6 devs.  In order to ensure that our dev workflow is successful and efficient, we need to establish a Continuous Integration and Continuous Deployment pipeline.

## CI Setup for Python:

1. Linting:  Linting helps us catch stylistic error as well as potential bugs early.  While stylistic rules on the  surface might not appear crucial when working solo, they become essential for teams as it facilitates the merging process by ensuring that each developer follows the same guidelines.  On popular framework for linting in Python is called **Flake8**.
2. Testing: Automated testings is critical to ensure that the application functions as expected upon deployment.  **Pytest** is an example of a framework used in the Python ecosystem to run those tests, and allows to write unit tests.
3. Building:  Python doesn't require compilation in the traditional sense because it is an interpreted language.  building might involve packaging the application or creating Docker images. **Setuptools** and **Docker** can be used to manage these tasks effectively.

## Alternatives to Jenkins or Github Actions

While they are both popular tools (I've used Github actions myself countless times because of how seamless it is), here are some alternatives I've found:

* GitLab CI/CD
* CircleCI
* Travis CI

## Self-Hosted v.s Cloud-based CI Environment

Here are some considerations a team might want to think about when choosing between a self-hosted or cloud-based solution.

* **Self-Hosted CI:**  Offers more control and can be more effective in the long run, especially if the organization has existing infrastructure.  However it does require a lot more maintenance and infrastructure management.
* **Cloud-based CI:** Easier to set up and scale and has better support and reduced operational overhead.  Cloud-based CI has been my personal go-to due to its easy of setup.  I've used Vercel as part of my main CI flow as they as the most obvious option for my NextJS projects, but I've also used Netlify for some projects before.  Due to the small-scale of my projects, it's been very cost effective (virtually free) to deploy and host my small web app projects.


Total: 365 words