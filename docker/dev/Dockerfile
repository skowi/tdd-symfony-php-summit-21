FROM expense-base

RUN pecl install pcov \
  && docker-php-ext-enable pcov

COPY vhost.conf /etc/apache2/sites-available/expense.conf
RUN a2ensite expense

RUN mv "$PHP_INI_DIR/php.ini-development" "$PHP_INI_DIR/php.ini"