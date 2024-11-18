# Kir Yaschenko

![Photo of Kir Yaschenko](https://artdir.net/redesign/img/kir.jpg)

## Contact Information
- **Email:** kir@artdir.net
- **Telegram:** [t.me/@artdir](https://t.me/@artdir)
- **Discord:** @artdir1989

## Summary
Full-stack Python Developer with strong product background and 14 years of IT experience. Specialized in AI and bot development, combining extensive programming expertise with deep understanding of product development lifecycle. Proven track record in developing scalable applications, implementing machine learning solutions, and optimizing business processes through automation. Background in psychology enhances ability to create intuitive, user-centric solutions.

## Technical Skills
- **Languages**: 
  - Python (3.x, async/await, multithreading)
  - JavaScript (ES6+)
  - HTML5/CSS3
- **Frameworks & Libraries**:
  - Backend: FastAPI, Django, Flask
  - Frontend: React.js, Next.js
  - AI/ML: scikit-learn, TensorFlow, GPT integration
- **Databases**: 
  - PostgreSQL
  - SQLAlchemy ORM
  - Redis
- **DevOps & Tools**:
  - Git/GitLab (CI/CD pipelines)
  - Docker
  - Linux/Unix
- **Development Practices**:
  - Test-Driven Development (pytest)
  - Agile methodologies (Scrum, Kanban)
  - API Design (REST, GraphQL)

## Professional Experience

### Senior Full-stack Developer & Project Lead `2022 - 2024`
**LLC «Servizoriya»**
- Architected and implemented scalable educational platform using Python/FastAPI and React
- Led development of AI-powered teacher assistant processing 1000+ requests daily
- Optimized application performance resulting in 40% reduction in response time
- Technologies: Python, FastAPI, React, PostgreSQL, Docker, GPT-3.5
- Managed distributed team of 6 developers using Agile methodologies

### Independent Software Developer `2020 - 2022`
**Individual Entrepreneur**
- Developed custom AI solutions for business automation
- Created high-load chat bots serving 30,000+ users
- Implemented automated sales funnels with 62% conversion rate
- Technologies: Python async, Next.js, PostgreSQL, ML algorithms

### Technical Co-founder `2018 - 2020`
**LLC «Inself»**
- Developed and launched B2C/B2B products from concept to production
- Implemented microservices architecture for scalable solutions
- Technologies: Python, Django, React, Docker, CI/CD

### Technical Product Owner `2016 - 2018`
**LLC «Uroven90»**
- Led technical strategy and development of company products
- Implemented Agile practices improving delivery time by 35%
- Managed integration of ML algorithms into existing products

### Lead Developer `2010 - 2016`
**LLC «Svet Mayaka»**
- Developed core business applications and automation tools
- Optimized database performance and application architecture
- Implemented testing practices reducing bugs by 45%

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

## Recommendations from Entrepreneurs

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

## Languages
- Russian (Native)
- English (Technical/Written Professional, Basic Speaking)