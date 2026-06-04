# dashboard-aniversariantes
# 🎂 Dashboard de Aniversariantes – Mazzini

> **Ferramenta:** Power BI  
> **Contexto:** Desenvolvido durante o Programa Jovem Aprendiz em Business Intelligence na Mazzini (2024–2025)  
> **Público:** Equipe interna – colaboradores e repositores da Mazzini

## 🧩 O Problema
A Mazzini não tinha uma forma automatizada de identificar e celebrar os aniversariantes do dia. O controle era feito manualmente, o que frequentemente fazia com que datas passassem despercebidas.

## 💡 A Solução
Painel em Power BI com atualização automática diária que exibe o aniversariante do dia de forma visual e clara, sem qualquer intervenção manual.

O painel:
- Atualiza automaticamente todos os dias
- Destaca o nome e informações do aniversariante do dia
- Exibe os próximos aniversários para antecipação
- Filtra por mês de aniversário e mês de admissão

## 🛠️ Tecnologias
| Ferramenta | Uso |
|---|---|
| Power BI | Desenvolvimento do painel e visualizações |
| Power Query (M) | Tratamento da base de colaboradores |
| DAX | Lógica para identificar o aniversariante do dia |
| Excel | Base de dados dos colaboradores |

## ⚙️ Lógica DAX principal
```dax
Aniversariante Hoje = 
VAR DiaHoje = DAY(TODAY())
VAR MesHoje = MONTH(TODAY())
RETURN
    CALCULATE(
        COUNTROWS(Colaboradores),
        DAY(Colaboradores[DataNascimento]) = DiaHoje,
        MONTH(Colaboradores[DataNascimento]) = MesHoje
    )
```

## 📸 Preview
![Dashboard](./prints/dashboard_aniversariantes.png)

## 📈 Impacto
- Eliminou o processo manual de verificação de aniversários
- Garantiu que nenhuma data fosse esquecida pela equipe
- Aumentou o engajamento entre colaboradores e repositores

## 👤 Autor
**Andrey Brasiliano**  linkedin.com/in/andrey-brasiliano-silva-429ba8279?originalSubdomain=br






