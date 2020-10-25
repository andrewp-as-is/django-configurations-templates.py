<!--
https://readme42.com
-->


[![](https://img.shields.io/pypi/v/django-configurations-templates.svg?maxAge=3600)](https://pypi.org/project/django-configurations-templates/)
[![](https://img.shields.io/badge/License-Unlicense-blue.svg?longCache=True)](https://unlicense.org/)
[![](https://github.com/andrewp-as-is/django-configurations-templates.py/workflows/tests42/badge.svg)](https://github.com/andrewp-as-is/django-configurations-templates.py/actions)

### Installation
```bash
$ [sudo] pip install django-configurations-templates
```

#### Features
key | default value | env
-|-|-
`TEMPLATES_BACKEND` | `django.template.backends.django.DjangoTemplates` | `DJANGO_TEMPLATES_BACKEND`
`TEMPLATES_DIRS` | `os.path.join(BASE_DIR,'templates')` | `DJANGO_TEMPLATES_DIRS`
`TEMPLATES_APP_DIRS` | `True` | `('yes', 'y', 'true', '1')`
`TEMPLATES_OPTIONS` | |
`TEMPLATES_CONTEXT_PROCESSORS` | `[]`
`TEMPLATES_CONTEXT_PROCESSORS_FILE` | `None` | `DJANGO_TEMPLATES_CONTEXT_PROCESSORS_FILE`
`TEMPLATES_LOADERS` | `[]` |

##### `settings.py`
```python
from configurations import Configuration
from django_configurations_templates import TemplatesMixin

class Base(TemplatesMixin,Configuration):
    ...
```

```python
class Base(TemplatesMixin,Configuration):
    TEMPLATES_CONTEXT_PROCESSORS = [
        'django.template.context_processors.request'
    ]
```

```python
class Base(TemplatesMixin,Configuration):
    TEMPLATES_CONTEXT_PROCESSORS_FILE='context_processors.txt'
```

#### Links
+   [django-configurations](https://github.com/jazzband/django-configurations)

<p align="center">
    <a href="https://readme42.com/">readme42.com</a>
</p>
