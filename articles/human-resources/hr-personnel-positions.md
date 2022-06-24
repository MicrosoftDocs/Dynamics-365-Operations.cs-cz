---
title: Pozice
description: Tento článek popisuje koncepční prvky, které může obsahovat pozice. Poskytuje také příklady, které ukazují, jak můžete tyto prvky použít ve své organizaci.
author: twheeloc
ms.date: 06/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPosition, HcmPersonnelManagementWorkspace
audience: Application User
ms.author: twheeloc
ms.reviewer: twheeloc
ms.custom: 269054
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 9c97a96e27188d12b9c5e626613e18d54d6632c0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888723"
---
# <a name="positions"></a>Pozice


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tento článek popisuje koncepční prvky, které může obsahovat pozice. Poskytuje také příklady, které ukazují, jak můžete tyto prvky použít ve své organizaci.

Před vytvořením pozice je třeba nastavit úlohu. Některé údaje pozice, jako je oblast kompenzace, přiřazení pracovníka, doba trvání pozice a vztah hlášení, jsou účinné od data.

## <a name="general-information"></a>Obecné informace

Při vytváření pozice musíte vybrat úlohu. Z vybrané úlohy se automaticky vyplní následující informace:

- popis
- Druh práce
- Ekvivalent plného úvazku
- Skupina pracovních míst

Název pozice se používá k odkazu na titul zaměstnance. (Titul, který je uveden na zaměstnanci, se nepoužívá.) Názvy pozic by proto měly být co nejvíce standardizovány.

> [!NOTE]
> Pracovníka nelze přiřadit k pozici v den, který je před datem k dispozici pro přiřazení.
>
> Parametr na kartě **Pozice** stránky **Sdílené parametry lidských zdrojů** řídí chování přiřazení pracovníků. Vyberte jednu z následujících hodnot:
>
> - **Nikdy** – Nemůžete přiřazovat pracovníky k novým pozicím při vytváření pozic. Při vytváření pozic se čas a datum položky **K dispozici pro přiřazení** na kartě **Obecné** stránky **Pozice** automaticky nastavuje na datum a čas vytvoření.
> - **Niky** – Nemůžete přiřazovat pracovníky k novým pozicím při vytváření pozic. Pokud vyberete tuto možnost, musíte otevřít stránku **Pozice** pro každou novou pozici, jakmile bude k dispozici. Pak na kartě **Všeobecné** zadejte datum **K dispozici pro přiřazení** umožňující přiřazení pracovníků. Pokud vyberete tuto možnost, datum přiřazení pracovníka bude nastaveno na **Nikdy** ve výchozím nastavení při pokusu o přiřazení pracovníka.

## <a name="position-duration"></a>Doba trvání pozice

Každá pozice je účinná po určitou dobu, která se označuje jako doba trvání. Například můžete mít letní pozici s trváním od 1. května 2021 do 31. srpna 2021. Datum aktivace je datum, kdy je pozice v systému aktivní. Datum deaktivace je datum, kdy pozice již není v systému aktivní.

Upozorňujeme, že ani datum k dispozici pro přiřazení, ani datum přiřazení pracovníka nesmí být před datem aktivace. Pozice není považována za aktivní, dokud není dosaženo data aktivace. Přiřazení pracovníka navíc nemůže být pozdější než datum deaktivace.

## <a name="reports-to-position"></a>Podřízený pozice

Pozice jsou důležitým prvkem nižší úrovně hierarchie organizace. Na stránce **Pozice** můžete určit pozici, která je nadřízená vaší pozici. Po přiřazení pracovníka k pozici, která je podřízena jiné pozici, můžete vytvořit vztah vykazování mezi zaměstnanci, kteří jsou přiřazeni do těchto dvou pozic. Například pozice 000220 je podřízená pozici 000300. Kim Akers je přiřazen na pozici 000220 a Sanjay Patel je přiřazen na pozici 000300. Kim Akers je proto podřízený Sanjayi Patelovi.

> [!TIP]
> Pozice podřízený se používá v celém systému k určení, kdo je manažerem zaměstnance. V předchozím příkladu, pokud je role manažera přiřazena Sanjayi Patelovi v systému, uvidí Kima Akerse jako přímého podřízeného v samoobsluze manažera. Vztah podřízenosti lze také použít při vytváření pravidel směrování pracovního postupu a úkolů kontrolního seznamu.

## <a name="relationships"></a>Vztahy

Pokud vaše organizace používá hierarchii matic nebo jinou vlastní hierarchii, můžete nastavit typy hierarchie pozic. Potom můžete přidat vztahy podřízenosti k pozicím pro každý typ hierarchie, který jste nastavili. Například Lori Penor je hlavní manažer společnosti Adventure Works a je přiřazená na pozici **Generální ředitel**. Lori spravuje vývoj produktu, který slouží k vymazání pomůcek. Vyžaduje účetní, který jí pomůže s financemi. Proto najala Kim Akersovou jako svého účetního. Kim je podřízena přímo Sanjay Patalovi, ale také pracuje s Lori Penorovou na práci související s financemi pro vývoj produktu pro čištění pomůcek.

V předchozím příkladu byste při nastavení pracovních vztahů mezi Kim Akersovou a Lori Penorovou provedli následující úkony:

1. Vytvoření vlastního typu hierarchie pozice s názvem **Pomůcka** pro vytvoření hierarchie, která zahrnuje pozice odpovědné za práci na produktu pro čištění pomůcek.
2. Určení pozice **Generální ředitel** na pozici, která je nadřazena pozici Kim v hierarchii **Pomůcka**.
3. Použití hierarchie pozic pro zobrazení struktury hlášení pozic. Pokud máte více hierarchií pozic, můžete zobrazit hierarchii pro každý typ hierarchie v hierarchii pozic. Dále můžete vyhledávat pozici podle ID pozice nebo podle jména pracovníka, který je přiřazený na pozici. Hierarchie pozice je organizační hierarchie.

## <a name="labor-union"></a>Odbor

Můžete zaznamenat, zda je pro danou pozici vyžadována odborová dohoda a který odborový svaz se používá. Dohodu můžete také spojit s právnickou osobou.

## <a name="financial-dimensions"></a>Finanční dimenze

Když vytváříte finanční dimenzi pro pozici, musíte určit právnickou osobu. Můžete vybrat výchozí dimenze pro každou dimenzi zvlášť. Alternativně můžete vybrat distribuční šablonu pro automatické vyplnění výchozích dimenzí. Distribuční šablona také poskytuje možnost přidělit částky mezi více hodnot dimenzí.
