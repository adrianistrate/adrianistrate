### Hi there 👋 

![Hiring Status](https://img.shields.io/badge/Hireable-true-green)

![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=adrianistrate&count_private=true&show_icons=true&theme=radical&hide=contribs,prs,issues)

```php
<?php

namespace App\DevsToHire;

#[Required]
class AdrianIstrate extends FlexibleDeveloper implements HumanInterface
{
    use Symfony;
    use RDBMS;
    use NoSQL;
    use Frontend;
    use Css;

    private static ?AdrianIstrate $instance = null;

    public function __construct(private string $firstName, private string $lastName)
    {

    }

    public static function getInstance(): AdrianIstrate
    {
        if (self::$instance === null) {
            self::$instance = new self('Adrian', 'Istrate');
            self::$instance
                ->setSymfonyAdoptionYear(2009)
                ->setSymfonyVersions([Symfony::VERSION_1, Symfony::VERSION_2, Symfony::VERSION_3, Symfony::VERSION_4, Symfony::VERSION_5, Symfony::VERSION_6])
                ->setRDBMS([RDBMS::MySQL, RDBMS::PostgreSQL, RDBMS::SQLite, RDBMS::MariaDB])
                ->setNoSQL([NoSQL::MongoDB], Level::BEGINNER)
                ->setFrontend([Frontend::REACT], Level::BEGINNER)
                ->enableSassLoader(Css::SCSS)
                ->setGlobalMotivationLevel('+Inf]')
                ->setGoal('Help startups and enterprises to build their products and services faster and better.');
        }

        return self::$instance;
    }
}
```