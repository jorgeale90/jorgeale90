<table>
<tr>
<td width="34%" valign="top">

```php
enum Platforms
{
    case Linux;
    case Docker;
    case Web;
    case WSL2;
}
```

```php
enum Backend: string
{
    case PHP     = '7 / 8';
    case Symfony = '4 / 5 / 6';
    case Laravel = 'latest';
    case Yii     = '1.x';
    case REST    = 'API Design';
    case PHPUnit = 'testing';
}
```

```php
enum Frontend: string
{
    case Vue        = '2 / 3';
    case Vuex       = 'store';
    case Pinia      = 'store';
    case JavaScript = 'ES6+';
    case TypeScript = 'basic';
    case Twig       = 'templates';
    case Playwright = 'E2E';
}
```

```php
enum Databases
{
    case PostgreSQL;
    case MySQL;
    case SQLite;
    case Redis;
}
```

```php
enum Geospatial
{
    case ArcGIS_Maps_SDK;
    case Google_Maps_API;
}
```

```php
enum Infrastructure
{
    case RabbitMQ_AMQP;
    case Docker;
    case Git;
    case Supervisor;
    case GNU_Linux;
}
```

```php
enum Languages: string
{
    case Spanish = 'native';
    case English = 'professional';
    case Italian = 'B1/B2';
}
```

```php
enum Profile
{
    case Rigorous;
    case TeamPlayer;
    case TestingBeliever;
    case AuditGradeQuality;
}
```

</td>
<td width="66%" valign="top">

```php
<?php

/**
 * Full-Stack Developer with 10+ years building production
 * web applications for critical-sector clients: fire department
 * management, public health and government systems.
 *
 * Open to REMOTE and RELOCATION opportunities in Europe 🇪🇺
 */
final class Information
{
    public string $name     = 'Jorge Cruz Borges';
    public string $title    = 'Full-Stack Software Developer';
    public string $email    = 'jorgealec90@gmail.com';
    public string $phone    = '+971 56 292 6420';
    public string $linkedin = 'linkedin.com/in/jorge-cruz-borges';
    public string $github   = 'github.com/jorgeale90';
    public array  $location = ['Sharjah', 'UAE 🇦🇪'];
}
```

```php
final class Education extends UniversidadDeOriente
{
    private function computerEngineering(): Degree
    {
        $level = 'Bachelor\'s Degree';
        $date  = Range::between('Sep 2009', 'Jul 2014');
        $core  = ['Software Development', 'OOP',
                  'Data Structures', 'Databases', 'Networking'];
    }
}
```

```php
final class Experience
{
    public function firstDue(): FullStackDeveloper
    {
        $date  = Range::between('Dec 2023', 'today');
        $stack = [Yii::class, Vue2::class, RabbitMQ::class,
                  PostgreSQL::class, ArcGIS::class];

        /* Fire department platform used across US agencies.
         * → Architected full audit-trail system: RabbitMQ/AMQP
         *   consumers with ACK/NACK, solved race conditions
         *   between async queues and PostgreSQL transactions.
         * → Killed N+1 queries migrating ActiveRecord to raw SQL.
         * → Vue.js inspection modules, geospatial layers with
         *   ArcGIS SDK + Google Maps, PHPUnit + Playwright E2E. */
    }

    public function freelance(): FullStackDeveloper
    {
        $date     = Range::between('Jan 2018', 'Nov 2023');
        $projects = [
            'CLIO'            => 'museum control · Symfony 4',
            'Sabio'           => 'public health · Symfony 5',
            'MenuTo-Go'       => 'restaurant SaaS · Symfony 6',
            'Digital Finance' => 'accounting · Symfony + Vue',
        ];

        /* 4 production systems for public-sector
         * and SMB clients, built end-to-end. */
    }

    public function ministryOfInformation(): SystemEngineer
    {
        $date = Range::between('Sep 2014', 'Jan 2018');

        /* Critical government infrastructure:
         * cryptographic systems and secure internal apps,
         * introduced automated testing practices. */
    }
}
```

</td>
</tr>
</table>

<div align="center">

<a href="https://linkedin.com/in/jorge-cruz-borges"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
<a href="mailto:jorgealec90@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white"/></a>
<img src="https://komarev.com/ghpvc/?username=jorgeale90&style=for-the-badge&color=555&label=VISITORS"/>

</div>
