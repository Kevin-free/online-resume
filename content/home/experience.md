+++
# Experience widget.
widget = "experience"  # See https://sourcethemes.com/academic/docs/page-builder/
headless = true  # This file represents a page section.
active = true  # Activate this widget? true/false
weight = 40  # Order that this section will appear.

title = "Experience"
subtitle = ""

# Date format for experience
#   Refer to https://sourcethemes.com/academic/docs/customization/#date-format
date_format = "Jan 2006"

# Experiences.
#   Add/remove as many `[[experience]]` blocks below as you like.
#   Required fields are `title`, `company`, and `date_start`.
#   Leave `date_end` empty if it's your current employer.
#   Begin/end multi-line descriptions with 3 quotes `"""`.
[[experience]]
  title = "Software Engineer"
  company = "Shenzhen Fist Bump Technology Co., Ltd."
  company_url = "https://fistbumpgame.com/"
  location = "Shenzhen, Guangdong, China"
  date_start = "2022-03-01"
  date_end = ""
  description = """
<img data-src="/media/fsbm.jpg" alt="fsbm" style="padding-bottom: 30px;" class="lazyload">

- Lead the design and development of the business analysis system, aggregate and analyze the log data of the game business and provide an API query interface, so that operators can view analysis indicators on the web and formulate strategies to optimize products.
- Use Golang and Kratos framework for rapid development, Redis and MySQL for data storage, ClickHouse for data analysis, use GitLab CI/CD + systemd to deploy on Alibaba Cloud machines.
- Use ELK to build a log analysis platform, and set up an error log panel for developers to expose problems in advance to avoid risks.

"""

[[experience]]
  title = "Software Engineer"
  company = "Shenzhen Fire Element Network Technology Co., Ltd."
  company_url = "http://www.huoys.com"
  location = "Shenzhen, Guangdong, China"
  date_start = "2021-04-01"
  date_end = "2022-01-01"
  description = """
<img data-src="/media/hys.jpg" alt="hys" style="padding-bottom: 30px;" class="lazyload">

-	As the first product of the company to enter the blockchain game, rowing game has transferred more than 50 selected personnel to set up a new department. I am mainly responsible for the development of background services, including the development of auction services and blind box services, and the development of infrastructure and optimization, and DevOps for the entire project.
-	Use Golang and Kratos to develop microservices from 0 to 1, use Redis and MySQL to store data, GitLab as CI/CD, Docker and K8s as deployment environment.
-	Combined with zaplog to optimize the log library and improve the overall performance of the service. Standardize DevOps processes and enhance system stability through automation.

"""

[[experience]]
  title = "Software Engineer"
  company = "Jiangxi Zonst Group Co., Ltd.	"
  company_url = "https://www.zonst.com/"
  location = "Nanchang, Jiangxi, China"
  date_start = "2020-05-01"
  date_end = "2021-04-01"
  description = """
<img data-src="/media/zonst.jpg" alt="zonst" style="padding-bottom: 30px;" class="lazyload">

-	As an important part of the company's main business of chess and card games - robot AI, its performance affects the player's experience and the company's revenue. I am mainly responsible for the development and optimization of robot AI algorithms in overseas mahjong projects.
-	Use Golang to combine data structure and algorithm knowledge to develop the robot's card-drawing and card-playing algorithm, and to develop the robot's difficulty level grading mechanism.
-	Through sync.Map and memorized search, the robot's card recommendation algorithm is optimized, which increases the efficiency by nearly 5 times, greatly improves the user experience and saves server overhead.

"""

+++
