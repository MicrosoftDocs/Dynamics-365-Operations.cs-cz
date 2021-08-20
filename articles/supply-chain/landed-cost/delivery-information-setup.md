---
title: Nastavení informací o doručení
description: Toto téma popisuje, jak nastavit informace o dodání pro modul nákladů za doručení.
author: sherry-zheng
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMPortTable, ITMLeadTimeTable, ITMLegTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: c9e36bef0b4cf87fa3fbad5d191731b48221a41e9d92241733e1bc3edb2ca838
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747004"
---
# <a name="delivery-information-setup"></a>Nastavení informací o doručení

[!include [banner](../../includes/banner.md)]

Toto téma popisuje, jak nastavit informace o dodání pro modul **Náklady za doručení**.

## <a name="shipping-ports"></a>Výchozí přístavy

Přepravní přístavy identifikují, odkud a kam je zboží přepravováno. Pro každou cestu je definován přístav „do“ a přístav „od“, a to na základě cesty vybrané pro plavbu. Přepravní přístavy se používají k vybudování úseků cesty a také aktivit během plavby. Obvykle jsou definovány pomocí názvu města a země nebo regionu, kde se nachází fyzický přepravní přístav.

Chcete-li pracovat s přepravními přístavy, přejděte na uzel **Náklady za doručení \> Nastavení informací o doručení \> Přepravní přístavy**. Zde můžete prohlížet, přidávat a odebírat záznamy o vašich přepravních přístavech. V následující tabulce jsou popsána pole, která jsou k dispozici pro každý záznam.

| Pole | popis |
|---|---|
| Výchozí přístavu | Zadejte jedinečný identifikační název/číslo přepravního přístavu. |
| popis | Zadejte popis přepravního přístavu. |

## <a name="tracking-control-center"></a><a name="tracking-control-center"></a>Centrum kontroly sledování

V řídicím centru sledování nastavíte doby realizace, aktualizace stavu a tok informací, které jsou spojeny s cestou, jak se přepravní kontejnery pohybují mezi jednotlivými úseky. Když vytvoříte řídicí záznam sledování, je spojen s konkrétním úsekem trasy cesty. Když cesta aktualizuje úsek, přidružený záznam bude aktualizován a vyplněn podle definice. Informace o sledování jednotlivých cest můžete aktualizovat na stránce **Všechny cesty**.

Chcete-li otevřít řídicí centrum sledování, přejděte na uzel **Náklady za doručení \> Nastavení informací o doručení \> Řídicí centrum sledování**.

Řídicí centrum sledování ukazuje jedno ze tří zobrazení stránky, v závislosti na hodnotě vybrané v poli **Typ vytvoření** v podokně seznamu: *Prázdný*, *Dodací lhůta* nebo *Aktualizace stavu*. Každý typ vytvoření aktualizuje jinou sadu informací, která je přidružena k postupu cesty z výchozího místa do konečného cíle.

### <a name="common-rule-settings"></a>Nastavení společných pravidel

Následující tabulka ukazuje pole, která jsou k dispozici pro všechny tři typy vytváření v řídicím centru sledování.

| Pole | popis |
|---|---|
| Zdrojová tabulka, zdrojové pole | Tato pole identifikují zdrojovou tabulku a pole v databázi. Pravidlo načte hodnotu v poli a poté ji použije způsobem, který je definován v jiných nastaveních pravidla. |
| Cílová tabulka, cílové pole | Tato pole identifikují cílovou tabulku a pole v databázi. Pravidlo načte hodnotu v poli a poté ji použije (nebo přepíše) způsobem, který je definován v jiných nastaveních pravidla. |
| Aktivita | Toto pole určuje typ aktivity, která by měla být použita na přepravní kontejner odpovídající pravidlu. |
| Odpovídající kritéria | Toto pole určuje, jak systém identifikuje shodu s pravidlem. U každé instance systém zkontroluje data ve zdrojové a cílové tabulce, aby určil, zda a kdy má být pole v cílové tabulce aktualizováno.<p>Například zdrojová tabulka je *Cesty* a cílová tabulka je *Záhlaví nákupu* nebo *Řádky nákupu*. Tabulka *Cesty* má v poli **Z přístavu** hodnotu *Hongkong* a tabulka *Záhlaví nákupu* má v poli **Z přístavu** hodnotu *Šanghaj*. Poté se vytvoří pravidlo, které má *Hongkong* jako přístav „z“. V tomto případě hodnoty pole **Kritéria shody** budou fungovat následujícím způsobem:</p><ul><li>**Obě** – Cílové pole nebude aktualizováno, protože jeden ze dvou přístavů se neshoduje.</li><li>**Zdroj** – Cílové pole bude aktualizováno, protože přístav „z“ zdrojové tabulky je *Hongkong*.</li><li>**Cíl** – Cílové pole nebude aktualizováno, protože přístav „z“ cílové tabulky je *Šanghaj* (ne *Hongkong*).</li></ul> |
| Kopírovat akci | Dostupné hodnoty jsou *Kopírovat* a *Výchozí*. Vyberte *Kopírovat*, chcete-li zkopírovat hodnotu ve zdrojovém poli do cílového pole. Vyberte *Výchozí*, chcete-li nastavit statickou hodnotu pro cílové pole. |
| Výchozí | Když je pole **Kopírovat akci** nastaveno na *Výchozí*, pole **Výchozí** definuje výchozí hodnotu cílového pole. Například pokud akce souvisí s aktualizací přístavu a pole **Kopírovat akci** je nastaveno na *Výchozí*, pole **Výchozí** identifikuje přístav. |
| Úsek | Toto pole identifikuje úsek cesty, ve kterém dojde ke specifikované akci, jako je nakládka nebo proclení. |
| Poskytovatel služby | Pokud je pro aktuální aktualizaci stavu/úseku cesty použit konkrétní poskytovatel služeb, toto pole identifikuje poskytovatele služeb. Poskytovatelé služeb jsou definováni v účtu dodavatele. |

### <a name="lead-time-rules"></a>Pravidla doby realizace

Doba realizace je odhadovaný čas potřebný k dokončení definovaného úseku cesty. Doba realizace každého úseku cesty se používá k výpočtu předpokládaného data dodání cesty. Toto datum se poté zapíše do pole **Potvrzené datum dodání** na každém nákupním řádku v cestě.

Ke správě aktualizací datumů používáte pravidla doby realizace. Aktivity se automaticky generují, když se pro cestu použije šablona cesty.

Chcete-li do řídicího centra sledování přidat pravidlo doby realizace, postupujte takto.

1. Proveďte jeden z následujících kroků:

    - Přejděte do uzlu **Náklady za doručení \> Nastavení cesty s více úseky \> Úseky**. Vyberte úsek, pro který chcete nastavit doby realizace, a poté v podokně akcí vyberte možnost **Řídicí centrum sledování**. Řídicí centrum sledování má předem načteno informace o vybraném úseku.
    - Přejděte do uzlu **Náklady na doručení \> Nastavení informací o doručení \> Řídicí centrum sledování**. Potom musíte ručně vybrat úsek v kroku 4 tohoto postupu.

1. V podokně seznamu nastavte **Typ vytvoření** na *Doba realizace*.
1. V podokně akcí zvolte **Nový**.
1. Pokud jste začali z řídicího centra sledování v kroku 1, nastavte pole **Úsek** na úsek, pro který chcete vytvořit pravidlo doby realizace. Pokud jste začali na stránce **Úseky**, pole **Úsek** je přednastaveno na úsek, který jste vybrali před otevřením řídicího centra sledování.

    Na základě hodnoty pole **Úsek** se automaticky nastaví několik polí, jak je znázorněno zde:

    - **Zdrojová tabulka:** *Kontejnerové aktivity*
    - **Zdrojové pole:** *Datum zahájení*
    - **Cílová tabulka:** *Kontejnerové aktivity*
    - **Cílové pole:** *Odhadované datum ukončení*

1. V poli **Aktivita** vyberte aktivitu, na kterou by se aktuální pravidlo mělo vztahovat.
1. Do pole **Doba realizace** zadejte čas realizace (ve dnech), který by se měl použít při spuštění aktuálního pravidla.

### <a name="status-update-rules"></a>Pravidla aktualizace stavu

Záznamy, kde je pole **Typ vytvoření** nastaveno na *Aktualizace stavu*, aktualizují stav řádků nákupní objednávky nebo stav na úrovni cesty, přepravního kontejneru nebo folia. Stavy lze nastavit nezávisle. Použijte je k informování uživatele nebo oddělení o fázi cesty (například o přijatých dokladech nebo přepravovaném zboží).

Když je pole **Typ vytvoření** nastaveno na *Aktualizace stavu*, řídicí centrum sledování obsahuje záložku **Řádky**, kde můžete definovat nákladovou oblast a aktualizovaný stav cesty. Například máte řádek, ve kterém je pole **Nákladová oblast** nastaveno na *Kontejner* a pole **Stav cesty** nastaveno na *Zboží v přepravě*. V tomto případě, když objednávka dokončí stanovený úsek, pole **Stav cesty** přepravního kontejneru bude aktualizováno na *Zboží na cestě*.

Aktualizace stavu poskytují stav cesty během různých řádků cesty a nákupní objednávky, které jsou s touto cestou spojeny. Jak cesta probíhá z výchozího přístavu, úseků cesty a celního odbavení až do cílového skladu, poskytuje pole záznamu cesty **Stav cesty** rychlý pohled na fázi, ve které se položky nacházejí.

Chcete-li do řídicího centra sledování přidat pravidlo aktualizace stavu, postupujte takto.

1. Proveďte jeden z následujících kroků:

    - Přejděte do uzlu **Náklady za doručení \> Nastavení cesty s více úseky \> Úseky**. Vyberte úsek, pro který chcete nastavit aktualizaci stavu, a poté v podokně akcí vyberte možnost **Řídicí centrum sledování**. Řídicí centrum sledování má předem načteno informace o vybraném úseku.
    - Přejděte do uzlu **Náklady na doručení \> Nastavení informací o doručení \> Řídicí centrum sledování**. Potom musíte ručně vybrat úsek v kroku 4 tohoto postupu.

1. V podokně seznamu nastavte **Typ vytvoření** na *Aktualizace stavu*.
1. V podokně akcí zvolte **Nový**.
1. Pokud jste začali z řídicího centra sledování v kroku 1, nastavte pole **Úsek** na úsek, pro který chcete vytvořit pravidlo aktualizace stavu. Pokud jste začali na stránce **Úseky**, pole **Úsek** je přednastaveno na úsek, který jste vybrali před otevřením řídicího centra sledování.

    Na základě hodnoty pole **Úsek** se automaticky nastaví několik polí, jak je znázorněno zde:

    - **Zdrojová tabulka:** *Kontejnerové aktivity*
    - **Zdrojové pole:** *Skutečné datum ukončení*
    - **Cílová tabulka:** Toto pole je prázdné.
    - **Cílové pole:** Toto pole je prázdné.

1. V poli **Aktivita** vyberte aktivitu, na kterou by se vaše pravidlo mělo vztahovat.
1. Na záložce **Řádky** zapište aktualizace stavu pro každou nákladovou oblast.

### <a name="blank-type-rules"></a>Pravidla prázdného typu

Používáte záznamy, které mají v poli **Typ vytvoření** hodnotu *Prázdný* pro přepsání nebo zadání hodnoty pole na základě údajů jiného pole. Pole z Nákladů za doručení přepíše data v jiných oblastech Microsoftu Dynamics 365 Supply Chain Management na základě pravidel, která jsou nastavena v řídicím centru sledování.

1. Přejděte do uzlu **Náklady na doručení \> Nastavení informací o doručení \> Řídicí centrum sledování**.
1. V podokně seznamu nastavte **Typ vytvoření** na *Prázdný*.
1. V podokně akcí zvolte **Nový**.
1. Definujte zdrojové a cílové hodnoty, kritéria shody, akci kopírování a další relevantní parametry, jak to vyžaduje vaše pravidlo.

### <a name="required-tracking-control-setup"></a>Požadované nastavení kontroly sledování

Pro každou šablonu cesty musí být v řídicím centru sledování nastaveny dva záznamy. Oba tyto záznamy mají v poli **Typ vytvoření** hodnotu *Prázdný* a používají se ve všech implementacích nákladů za doručení. Pomáhají zajistit, aby datum potvrzení nákupu a očekávaná data zboží v přepravě byla aktualizována očekávaným způsobem pro cesty a související řádky nákupní objednávky.

K aktualizaci řádků nákupu je vyžadován první záznam. Musí mít následující nastavení:

- **Zdrojová tabulka:** *Kontejnerové aktivity*
- **Zdrojové pole:** *Odhadované datum ukončení*
- **Cílová tabulka:** *Nákupní řádky*
- **Cílové pole:** *Potvrzeno nebo datum dodání*

Druhý záznam je nutný k aktualizaci zboží v přepravních transakcích. Musí mít následující nastavení:

- **Zdrojová tabulka:** *Kontejnerové aktivity*
- **Zdrojové pole:** *Odhadované datum ukončení*
- **Cílová tabulka:** *Objednávka přepravovaného zboží*
- **Cílové pole:** *Očekávané datum*
