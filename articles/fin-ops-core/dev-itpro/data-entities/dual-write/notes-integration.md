---
title: Integrace poznámek
description: Toto téma popisuje integraci dat poznámek v duálním zápisu.
author: RamaKrishnamoorthy
ms.date: 02/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: ceb5b7c90cc7efa0049d0278e2c245228e5b52bd
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186779"
---
# <a name="note-integration"></a>Integrace poznámek

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Během obchodních procesů Microsoft Dynamics 365 uživatelé často shromažďují informace o svých zákaznících. Tyto informace se zaznamenávají jako aktivity a poznámky. Toto téma popisuje integraci dat poznámek v duálním zápisu.

Informace o zákaznících lze klasifikovat následujícími způsoby:

+ **Akční informace, které uživatel Dynamics 365 zpracovává jménem zákazníka** – Například společnost Contoso (uživatel Dynamics 365) pořádá televizní soutěž. Jeden ze zákazníků společnosti Contoso (zákazník) se chce televizní soutěže zúčastnit. Zákazník požádá zaměstnance společnosti Contoso, aby mu rezervoval slot v televizní soutěži. Rezervace probíhá v kalendáři účastníka akce společnosti Contoso.
+ **Akční informace pro uživatele Dynamics 365** – Například zákazník, který kupuje jednotku Surface, zadá speciální pokyny, které označují, že by zařízení mělo být před dodáním zabaleno v dárkovém balení. Tyto pokyny jsou akční informace, s nimiž by měl zacházet zaměstnanec společnosti Contoso odpovědný za balení.
+ **Neakční informace** – Například zákazník navštíví obchod Contoso a během rozhovoru se spolupracovníkem obchodu projeví zájem o hry a herní příslušenství *Halo*. Obchodník si tyto informace poznamená. Nástroj pro doporučení produktu jej poté použije k doporučení zákazníkovi.

Obecně jsou akční informace zachyceny jako *činnosti* v aplikacích Finance and Operations a aplikacích Customer Engagement. Neakční jsou informace zachyceny jako *poznámky* v aplikacích Finance and Operations a *anotace* v aplikacích Customer Engagement.

> [!TIP]
> Ačkoli poznámky jsou určeny pro neaktivní informace, aplikace vám nebudou bránit v jejich použití k ukládání a zpracovávání akčních informací, pokud je chcete použít tímto způsobem.

Společnost Microsoft v současné době vydává funkce pro integraci poznámek. (Funkce pro integraci aktivit bude uvolněna později.) Integrace poznámek je k dispozici pro zákazníky, dodavatele, prodejní objednávky a nákupní objednávky.

## <a name="create-a-note-in-a-customer-engagement-app"></a>Vytvoření poznámky v aplikaci Customer Engagement

Chcete-li vytvořit poznámku v aplikaci Customer Engagement a poté ji synchronizovat do aplikace Finance and Operations, postupujte podle těchto kroků.

1. V aplikaci Customer Engagement otevřete záznam účtu pro zákazníka.
2. V podokně **Časová osa** vyberte znaménko plus (**+**) a poté vyberte **Poznámka** k vytvoření poznámky.

    ![Vytvoření poznámky v aplikaci Customer Engagement](media/notes-ce-1.png)

3. Zadejte název a popis a poté vyberte **Přidat poznámku**.

    ![Zadání nadpisu a popisu](media/notes-ce-2.png)

    Nová poznámka se přidá na časovou osu zákazníka.

    ![Nová poznámka na časové ose zákazníka](media/notes-ce-3.png)

4. Přihlaste se do aplikace Finance and Operations a otevřete stejný záznam zákazníka. Všimněte si, že tlačítko **Přílohy** (symbol kancelářské sponky) v pravém horním rohu označuje, že záznam má přílohu.

    ![Oznámení o příloze](media/notes-ce-4.png)

5. Vyberte tlačítko **Přílohy** pro otevření stránky **Přílohy**. Měli byste najít poznámku, kterou jste vytvořili v aplikaci Customer Engagement.

    ![Poznámka z aplikace Customer Engagement](media/notes-ce-5.png)

Všechny aktualizace poznámky se synchronizují tam a zpět mezi aplikací Finance and Operations a aplikací Customer Engagement.

## <a name="create-a-note-in-a-finance-and-operations-app"></a>Vytvoření poznámky v aplikaci Finance and Operations

Poznámku můžete vytvořit také v aplikaci Finance and Operations a poté ji synchronizovat do aplikace Customer Engagement.

Chcete-li vytvořit poznámku v aplikaci Finance and Operations a poté ji synchronizovat do aplikace Customer Engagement, postupujte podle těchto kroků.

1. V aplikaci Finance and Operations na stránce **Přílohy** vyberte **Nový** \> **Poznámka**.

    ![Vytvoření poznámky v aplikaci Finance and Operations](media/notes-fo-1.png)

2. Zadejte název a krátkou sadu pokynů a poté vyberte **Uložit**.

    ![Zadání nadpisu a pokynů](media/notes-fo-2.png)

3. V aplikaci Customer Engagement aktualizujte záznam. Na časové ose byste měli najít novou poznámku.

    ![Nová poznámka na časové ose v aplikaci Customer Engagement](media/notes-fo-3.png)

Poznámku můžete klasifikovat jako interní nebo externí.

- V aplikaci Finance and Operations na stránce **Přílohy** otevřete poznámku a poté v poli **Omezení** vyberte **Interní**, nebo **Externí**.

    ![Pole omezení](media/notes-fo-4.png)

Můžete také vytvořit adresu URL.

1. V aplikaci Finance and Operations na stránce **Přílohy** vyberte **Nový** \> **Adresa URL**.
2. Zadejte nadpis a adresu URL.
3. V poli **Omezení** pole, vyberte **Interní**, nebo **Externí**.

    ![Vytvoření adresy URL v aplikaci Finance and Operations](media/notes-fo-5.png)

4. Zvolte **Uložit**.

    Protože aplikace Customer Engagement nemají typ adresy URL, je adresa URL integrována s duálním zápisem jako poznámka.

    ![Adresa URL zobrazená jako poznámka v aplikaci Customer Engagement](media/notes-ce-6.png)

> [!NOTE]
> Přílohy souborů nejsou podporovány.

## <a name="templates"></a>Šablony

Integrace poznámek zahrnuje mapy kolekce tabulek, které pracují společně během interakce s daty odběratele, jak je uvedeno v následující tabulce.

| Aplikace Finance and Operations | Aplikace Customer Engagement | popis |
|----------------------------|-------------------------|-------------|
| [Přílohy zákazníků](mapping-reference.md#230) | Poznámky | Firmy, které používají prostý text a adresy URL k zachycení specifických informací o zákazníkovi (pro organizace i osoby). |
| [Přílohy dokumentu dodavatele](mapping-reference.md#231) | Poznámky | Firmy, které používají prostý text a adresy URL k zachycení specifických informací o dodavateli (pro organizace i osoby). |
| [Přílohy dokumentu záhlaví prodejní objednávky](mapping-reference.md#229) | Poznámky | Firmy, které používají k zachycení konkrétních informací o prodejní objednávce prostý text a adresy URL. |
| [Přílohy dokumentu záhlaví nákupní objednávky](mapping-reference.md#232) | Poznámky | Firmy, které používají k zachycení konkrétních informací o nákupní objednávce prostý text a adresy URL. |

## <a name="limitations"></a>Omezení

Jakmile nainstalujete řešení pro poznámky, nemůžete jej odinstalovat. 

Další informace viz [Odkaz na mapování duálního zápisu ](mapping-reference.md).
