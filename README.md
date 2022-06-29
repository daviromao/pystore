# Pystore: e-commerce with django

This project is a e-commerce builded with Django, Bootstrap and Docker.

# How to run the project

- Clone this repository:
```
git clone git@github.com:daviromao/pystore.git
```

- Setup containers:
```
docker-compose up --build
```

- Run the migrations:
```
docker-compose exec web python manage.py migrate
```

- Run the tests:
```
docker-compose exec web pytest
# algumas opções:
docker-compose exec web pytest -x --cov --cov-report=html
```

- Use the fixture `products.json` to load a sample data. To insert the products in db:
```
docker-compose exec web python manage.py loaddata products
```

- Create a superuser to get acess in admin page:
```
docker-compose exec web python manage.py createsuperuser
```

Por fim, acesse o site neste link: [http://localhost:8000/](http://localhost:8000/)

Qualquer dúvida é só me procurar.

# Referências

- [Livro Django for Professionals](https://djangoforprofessionals.com/)
- [Livro Django 3 By Example](https://www.packtpub.com/product/django-3-by-example-third-edition/9781838981952)
- [Livro Two Scoops of Django](https://www.feldroy.com/collections/two-scoops-press/products/two-scoops-of-django-3-x)
- [Livro A Wedge of Django](https://www.feldroy.com/collections/two-scoops-press/products/a-wedge-of-django)
- [Repostitório Cookiecutter Django](https://github.com/pydanny/cookiecutter-django)
