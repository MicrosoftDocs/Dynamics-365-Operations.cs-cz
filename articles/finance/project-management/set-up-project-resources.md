---
title: Nastavení prostředků projektu
description: Tohle téma poskytuje informace o nastavení nebo požadování prostředků projektu.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c882e23794e3937f85b3e73774b36deaf28ac3ed
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760498"
---
# <a name="set-up-project-resources"></a>Nastavení prostředků projektu

[!include [banner](../includes/banner.md)]

Musíte nastavit kalendář a přidružit jej se zaměstnancem nebo pracovníkem. Kalendář lze použít pro naplánování projektu a pracovní doby zdrojů, které jsou na projekt rezervovány. Během nastavení kalendáře může projektový manažer provádět vyrovnání zdrojů v rámci optimalizace zdrojů. Na základě plánu kalendáře lze na zdroje uvalit omezení. Můžete nastavit kalendář na stránce **Kalendáře**.

Pokud nastavíte pracovníka jako projektový zdroj, můžete se vybrat z pracovníků, kteří pracují ve společnosti, pro kterou nastavujete zdroje. Případně můžete vybrat pracovníky z ostatních společností ve vaší organizaci. Tito pracovníci se označují jako mezipodnikové zdroje.

Následující postupy vysvětlují, jak nastavit pracovníka jako zdroj projektu v rámci společnosti a jak nastavit mezipodnikový zdroj projektu.

## <a name="set-up-a-worker-as-a-project-resource"></a>Nastavení pracovníka jako prostředek projektu

1. Na stránce **Pracovníci** v seznamu **Pracovníci** vyberte pracovníka, kterého chcete přidat jako prostředek projektu, a otevřete záznam pracovníka.
2. V podokně akcí zvolte na **Projekt** &gt; **Nastavení** &gt; **Nastavení projektu**.
3. Vyberte kalendář a zavřete stránku.

Můžete také určit výchozí projekty pro prostředky jako typ předběžného přiřazení. Předběžné přiřazení lze použít, pokud manažer prostředků nebo projektu dopředu ví, na kterých projektech budou prostředky pracovat. Předběžné přiřazení může být založeno také na žádosti investora projektu nebo odběratele. Pokud chcete předběžně přiřadit projekt, na stránce **Přiřadit projekty** na kartě **Projekty** v seznamu **Zbývající projekty** vyberte příslušný projekt.

## <a name="set-up-an-intercompany-resource"></a>Nastavení mezipodnikového zdroje

Při nastavování pracovníka jako mezipodnikového zdroje je nutné dokončit nastavení ve společnosti poskytující půjčku a společnosti, která zažádala o půjčku.

### <a name="in-the-lending-company"></a>Ve společnosti poskytující půjčku

1. V aplikaci Finance ověřte, zda je vybrána společnost poskytující půjčku, a pak dokončete postup uvedený v předchozí části s názvem Nastavení pracovníka jako zdroje projektu.
2. Na stránce **Mezipodnikového účetnictví** vyberte **Nová**.
3. V poli **ID právnické osoby** vyberte společnost poskytující půjčku. Podle potřeby vyplňte zbývající pole a potom zvolte **Uložit**.
4. Na stránce **Mezipodniková cena** vyberte **Nová**.
5. V poli **Právnická osoba, která si půjčuje** vyberte příslušnou společnost.
6. Pokud si chcete od společnosti poskytující půjčku pouze vypůjčit zdroj, který jste vytvořili na začátku této části, v poli **Zdroj**, vyberte název zdroje, který jste vytvořili. Pokud chcete zpřístupnit všechny zdroje společnosti poskytující půjčku společnosti, která si půjčuje, ponechte pole **Zdroj** prázdné.
7. Na stránce **Parametry modulu Řízení a účetnictví projektu** na kartě **Mezipodnikové** nastavte možnost **Povolit mezipodnikové plánování prostředků a časové rozvrhy** na **Ano**.

### <a name="in-the-borrowing-company"></a>Ve společnosti, která zažádala o půjčku 

- Na stránce **Seznam zdrojů** ve filtru vyhledávání zadejte název zdroje, který jste vytvořili v předchozím postupu pro společnost poskytující půjčku, a ověřte, že název je zahrnut v seznamu zdrojů pro společnost, která žádá o půjčku.

## <a name="request-project-resources"></a>Žádost o prostředky projektu
Funkce pro plánování projektových zdrojů umožní pouze správcům zdrojů distribuovat personální zdroje na aktivity nebo projekty. Chcete-li povolit tuto funkci, proveďte následující úlohy nebo ověřte, že byly dokončeny:

- Nastavte číselné řady.
- Nastavte workflowy pro řízení a účetnictví projektu.
- Povolit workflowy žádosti o prostředek.

Po dokončení předcházejících úkolů můžete provést následující úkoly podle potřeby.

- Vytvořte požadavek na prostředek z předběžně definovaných personálních prostředků.
- Monitorujte požadavky na prostředky.
- Naplňte požadavky na prostředky
- Požádejte o personální prostředek z WBS.
- Zarezervujte si zdroje na projektu bez požadavku na personální prostředek.
