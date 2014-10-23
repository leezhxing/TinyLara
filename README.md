# *TinyLara*

```
  ______    _                      __                         
 /_  __/   (_)   ____    __  __   / /   ____ _   _____  ____ _
  / /     / /   / __ \  / / / /  / /   / __ `/  / ___/ / __ `/
 / /     / /   / / / / / /_/ /  / /___/ /_/ /  / /    / /_/ / 
/_/     /_/   /_/ /_/  \__, /  /_____/\__,_/  /_/     \__,_/  
                      /____/                                  
```

TinyLara is a simple PHP framework based on Composer, looks like a Lite Edition of Laravel.

## Start
### Download:
```
git clone https://github.com/TinyLara/TinyLara
cd TinyLara
```

### Install dependencies:

    composer update

Then modify `app/database.php` with right information and import `demo.sql`.

### See:

*config/routes.php :*
    
    Macaw::get('', 'HomeController@home');
    
*app/controllers/HomeController.php :*

    public function home()
    {
      // build view sample
      $this->view = View::make('home')->with('article',Article::first())
                                      ->withTitle('MFFC :-D')
                                      ->withFooBar('foo_bar');
      /*
      // build mail sample
      $this->mail = Mail::to(['ooxx@gmail.com', 'ooxx@qq.com'])
                          ->from('OOXX <ooxx@163.com>')
                          ->title('Foo Bar')
                          ->content('<h1>Hello~~</h1>');
      // redis sample
      Redis::set('key','value',3000,'ms');
      echo Redis::get('key');
      */
    }

### Run:
```
cd public && php -S 127.0.0.1:3000
```
Visit [http://127.0.0.1:3000/](http://127.0.0.1:3000/)

### It's already running!
<br>

## Features

1. Suer small (~150 LOC) router: fast and sexy [codingbean/macaw](codingbean/macaw)
2. MVC architecture
3. One of the Most powerful PHP ORM on Earth: [Laravel Eloquent](http://laravel.com/docs/4.2/eloquent)
4. Powerful Laravel-style views loader
5. Redis ready in Laravel-style
6. Handy SMTP mailer


## License

The TinyLara framework is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT)