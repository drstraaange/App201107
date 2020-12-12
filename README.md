# App201107

`pip freeze > requirements.txt` - 依存関係の出力


```python
class Snippet(models.Model):
    created = models.DateTimeField(auto_now_add=True)
    title = models.CharField(max_length=100, blank=True, default='')
    code = models.TextField()
    linenos = models.BooleanField(default=False)
    language = models.CharField(choices=LANGUAGE_CHOICES, default='python', max_length=100)
    style = models.CharField(choices=STYLE_CHOICES, default='friendly', max_length=100)

    class Meta:
        ordering = ['created']
```
summary

### フォーク元を最新する
upstream(フォーク元) ： https://github.com/drstraaange/App201107
origin(フォーク先) ： git@github.com:create-webapp-menbers/App201107.git

- フォーク元のリモートrepositoryを登録
- fetchする
- プル先を"upstream"に設定
- プル実行
- プル先を"origin"に設定
- プル実行
- 全て最新
