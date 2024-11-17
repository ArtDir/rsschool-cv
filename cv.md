# Kir Yaschenko

![Photo of Kir Yaschenko](https://artdir.net/redesign/img/kir.jpg)

## Contact Information
- **Email:** kir@artdir.net
- **Telegram:** [t.me/@artdir](https://t.me/@artdir)
- **Discord:** @artdir1989

## Summary
Product Owner with 14 years of IT experience transitioning to Python Full-Stack Development. Combining psychology background with practical programming skills in AI and bot development. Unique blend of product management expertise and technical capabilities allows creating efficient, user-centric solutions. Passionate about AI technologies and automation.

## Technical Skills
- **Programming Languages**: Python (async programming), JavaScript, HTML, CSS
- **Frameworks**: React JS, Next.js
- **Databases**: PostgreSQL
- **Tools**: Git/GitLab, Figma, Axure, Webflow, Adobe XD
- **Methodologies**: Agile (Scrum, Kanban, CusDev, Extreme programming)
- **Project Management**: Jira, Trello

## Soft Skills
- **Team Collaboration**: Conduct meetings, resolve conflicts, and have experience managing a distributed team of 24 people.
- **Requirements Gathering**: Collect and prioritize requirements from customers and stakeholders.
- **UX/UI Design**: Create user-friendly interfaces and conduct A/B testing to optimize user experience.

## Professional Experience
- `2022 - 2024` LLC «Servizoriya» — Project Manager: developed «Metaverse» and «Environment» products, created neural assistant for teachers
- `2020 - 2022:` Individual Entrepreneur: developed IT solutions, managed distributed teams
- `2018 - 2020` LLC «Inself» — Co-founder: launched B2C and B2B products
- `2016 - 2018` LLC «Uroven90» — Product Owner
- `2010 - 2016` LLC «Svet Mayaka» — Chief Developer

## Education and Qualifications
- **Southern Federal University**, Master of Psychological Sciences, Department of Management and Business.
- **Resident of** the Southern IT Park, IT Park of Kazan and Innopolis.
- **Completed the MiniMBA program** at Moscow Business School.
- **1st place in the «Editors' School»** at Artem Gorbunov's Bureau.
- **Courses on effective work with** distributed teams, leadership, conflict resolution, UX/UI prototyping, usability, CusDev, Kanban, agile development, extreme programming (XP), bot creation in VK, automated sales funnels, and basics of Python.

*Certificates of qualification improvement available upon request.*

## Key Projects

- [**Lively.ru**](https://lively.ru): Completed a turnkey project, assembled a team of 14 people, created 5 paid products and 50+ articles, tested sales funnels, and developed SEO and targeted advertising strategies.

- [**Neuro Freud AI bot**](https://vk.com/wall318680_15486): Developed an ironic bot that increased the number of comments by 23 times, conducted 3141 consultations, and left 215 links to paid products.

- [**Sreda AI Edu-platform**](https://sreda.works): Created an educational HR platform with individual learning paths for corporate clients, conducted usability tests, and set up promotion through Yandex.Direct.

- [**Pinator 3.0**](https://t.me/@yaboltun_bot): Developed a SaaS service for goal setting with over 30,000 bots created in VK, an automated sales funnel with a 62% conversion rate to subscription and 11% to sales.

- [**Metaverse Servisoria Land**](https://www.roblox.com/games/13340302526/Servisoria-Land): Created an educational gaming platform in Roblox with mechanics for completing the adaptation plan, implemented gamification elements, and presented at major conferences.

## Source Code

1. [Neural Psychologist Bot](https://gitflic.ru/project/artkir/neuro3) — AI project increasing social media reach through context-preserving conversations.
2. [Bitrix24 Automation](https://gitflic.ru/project/artkir/docs24) — AI that organizes addresses in Bitrix tables.
3. [Neuro Nastya](https://gitflic.ru/project/artkir/sreda-bot) — Telegram bot providing feedback to a learner based on a video lesson.
4. [Za Bota](https://gitflic.ru/project/artkir/zabota2) — Project liking and commenting based on user post topics.
5. [Geolocator](https://gitflic.ru/project/artkir/locator) — Next.js application grouping locations by proximity for a mystery shopper based on specified criteria.

*I work exclusively on commercial projects (some under NDA), repository access upon request.*

## Code Examples

### Example 1: Training a Machine Learning Model with scikit-learn (Python)

```python
from sklearn.datasets import load_iris
from sklearn.model_selection import train_test_split
from sklearn.neighbors import KNeighborsClassifier
from sklearn.metrics import accuracy_score

# Load the Iris dataset
iris = load_iris()
X, y = iris.data, iris.target

# Split the data into training and testing sets
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# Create and train the KNN classifier
knn = KNeighborsClassifier(n_neighbors=3)
knn.fit(X_train, y_train)

# Make predictions and evaluate accuracy
y_pred = knn.predict(X_test)
accuracy = accuracy_score(y_test, y_pred)
print(f'Model accuracy: {accuracy:.2f}')

```

### Example 2: Asynchronous Web Scraping (JavaScript)

```javascript
const axios = require('axios');
const cheerio = require('cheerio');

class WebScraper {
    // Function to scrape top repositories from GitHub
    async scrapeTopRepositories() {
        try {
            const response = await axios.get('https://github.com/trending');
            const $ = cheerio.load(response.data);

            const repositories = $('.Box-row').map((i, elem) => ({
                name: $(elem).find('h3').text().trim(),
                description: $(elem).find('p').text().trim(),
                stars: $(elem).find('a.muted-link').first().text().trim()
            })).get();

            return repositories.slice(0, 5);
        } catch (error) {
            console.error('Error during scraping:', error);
            return [];
        }
    }

    // Function to display trending repositories
    async displayTrending() {
        const repos = await this.scrapeTopRepositories();
        console.log('🔥 Top 5 GitHub Repositories:');
        repos.forEach((repo, index) => {
            console.log(`${index + 1}. ${repo.name}`);
            console.log(`   📝 ${repo.description}`);
            console.log(`   ⭐ ${repo.stars} stars\n`);
        });
    }
}

// Run the scraper
const scraper = new WebScraper();
scraper.displayTrending();

```

### Recommendations from Entrepreneurs

- [Ainur Abdulnasyrov](https://www.youtube.com/watch?v=KTBAZpi92LA&list=PLk1oPQ5FsFdmdurOhknixOhYxa6fxhpni) 
  - Founder of LinguaLeo (12 million users worldwide)
  - City: Kazan, Russia
  - Status: Successful Technology Entrepreneur

- [Azamat Ushanov](https://www.youtube.com/watch?v=CAPOyiy9cXc&list=PLk1oPQ5FsFdmdurOhknixOhYxa6fxhpni&index=2)
  - Most Famous Information Business Expert in Russia
  - City: Ufa, Russia
  - Status: Leader in Online Education

- [Leonid Egorov](https://www.youtube.com/watch?list=PLk1oPQ5FsFdmdurOhknixOhYxa6fxhpni&v=R8o69U25m1Y)
  - Entrepreneur
  - Director of Yuri Moroz Institute
  - City: Saint Petersburg, Russia

- [Oleg Ivanchikhin](https://www.youtube.com/watch?list=PLk1oPQ5FsFdmdurOhknixOhYxa6fxhpni&v=JyzCgyhyGMU)
  - Founder of Contact Technologies Group
  - City: Jerusalem, Israel
  - Status: International Entrepreneur

*To watch the video testimonial about Kir Yashchenko's work from the listed individuals, simply click on the link with their name.*