# React Native Challenge

Here is the React Native Challenge from YosemiteLabs. Working here, we expect you to learn new things and do a lot of research. We aim at big projects that might have complex challenges, and this test should give you an idea on what we expect you to do.

In this test, we aim:
- Allow you to work with international data that you probably never seen before
- Prove your React Skills by developing a simple App
- Prove your design skills

## Objective

You must create a React Native App that:

- Receive the CNPJ from the user, using an Input field, and format the CNPJ's 14 digits in a human readble format like: `xx.xxx.xxx/xxxx-xx`
- Integrate with `https://public.fluxoresultados.com.br/v1/cnpj/{cnpj}` API, sending the CNPJ in a number-only format like: `xxxxxxxxxxxxxx`
- Present the following fields to the user:
    1. `situacao` (Translated as "Status", can be ATIVA which means Active or INATIVA which means Inactive)
    2. `telefone` (Translated as "Phone Number")
    3. Count of `atividade_principal` array, translated as "Number of Activities"
    4. `capital_social` (Translated as "Initiial Income", its a monetary field, and should be formatted as Brazilian Reais (BRL))
    5. `fantasia` (Transalated as "Company Name")
    6. `nome` (Translated as "Company Legal Name")
    7. `ultima_atualizacao` (Translated as "Date of last update", its a date field and should be formatted)


Here is some Brazilian companies for you to test
- 60872504000123 -> Itaú Unibanco (Biggest brazilian private bank)
- 16501555000157 -> Stone (4th biggest brazilian payment company)
- 76801166000179 -> O Boticário (One of biggest beauty and cosmetic companies)

You can use any framework that you like (for example, you can use Expo to build your app). You also can use components libraries like React Native Paper and other Javascript libraries that you might find useful.

## Context on the data

Brazilian Companies are represented by a unique ID, called CNPJ. CNPJ is a 14 digits that is often presented in a formatted with points, slashes and bars. So for example the CNPJ `16501555000157` is presented to the user as  `16.501.555/0001-57`. You should format the CNPJ like this on your app (Input and Outputs).


## Grab CNPJ data

Your app must have an Input field that will allow the user to insert the company's CNPJ. That input should be masked, so the user will write the 14 digits of the CNPJ like `16501555000157` but it will be automatically formatted to `16.501.555/0001-57`.

After that you should run a GET request on the CNPJ api as presented by the cURL snippet bellow:

```
curl --request GET \
  --url https://public.fluxoresultados.com.br/v1/cnpj/16501555000157
```

## Parse the data

After you have access to the data, you should parse the fields, presenting them in a screen to the user. Here is where your design skills count, you should build a nice looking screen.

The fields that should be presented are:

1. `situacao` (Translated as "Status", can be ATIVA which means Active or INATIVA which means Inactive)
2. `telefone` (Translated as "Phone Number")
3. Count of `atividade_principal` array, translated as "Number of Activities"
4. `capital_social` (Translated as "Initiial Income", its a monetary field, and should be formatted as Brazilian Reais (BRL))
5. `fantasia` (Transalated as "Company Name")
6. `nome` (Translated as "Company Legal Name")
7. `ultima_atualizacao` (Translated as "Date of last update", its a date field and should be formatted)

Pay attention to the status, dates and numeric fields. It should be formatted to the user

## Conclusion

We expect this challenge to be done in a week. After you finishes, you can share the repository with the code with `brennoflavio` (github). Or send the code by email to brenno@yosemitelabs.com

Happy coding!
