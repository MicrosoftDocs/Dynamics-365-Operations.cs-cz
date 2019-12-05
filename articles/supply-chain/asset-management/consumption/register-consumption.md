---
title: Registrace spotřeby
description: Toto téma vysvětluje, jak registrovat spotřebu v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3d23375ec7ebe9b43c2d2e3e376e26c348131bd3
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812253"
---
# <a name="register-consumption"></a>Registrace spotřeby

[!include [banner](../../includes/banner.md)]

 

Když byla úloha údržby dokončena na pracovním příkazu, následující krok provede registraci spotřeby a zaúčtuje deníky. Registrace můžete provést u následujících typů spotřeby: hodiny, položky a výdaje. Různé typy spotřeby jsou registrovány a zaúčtovány na stránce **Deníky pracovních příkazů**. Nastavení deníku ve **Správě majetku** se používá k vytváření a zaúčtování samostatných deníků pro hodiny, položky a výdaje v modulu **Řízení a účetnictví projektu**.

Řádky prognózy můžete v některých případech přidávat nebo odstraňovat v rámci pracovního příkazu. Nastavení stavu životního cyklu pracovního příkazu, související typ projektu a pravidla fáze související s typem projektu určují, zda lze přidávat nebo upravovat řádky deníku. Další informace o stavech životního cyklu pracovního příkazu a souvisejících fázích projektu si můžete přečíst v tématu [Prognózy, pracovní příkazy a projekty](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).

>[!NOTE]
>Je možné nastavit automatické zaúčtování deníků ve stavu životního cyklu pracovního příkazu. Další informace najdete v části [Stavy životního cyklu pracovního příkazu](../setup-for-work-orders/work-order-lifecycle-states.md).

1. Klikněte na **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.

2. Vyberte pracovní příkaz a klikněte na položku **Deníky**.

3. Kliknutím na možnost **Kopírovat z prognózy** můžete převést řádky prognózy, které mohou být spojeny s daným pracovním příkazem. Můžete vybrat typy spotřeby, které chcete převést.

4. V případě potřeby můžete na příslušné pevné záložce přidat další řádky spotřeby kliknutím na položku **Přidat řádek** a vyplněním dat na řádku.

5. Kliknutím na možnost **Ověřit deníky** ověřte řádky deníku před zaúčtováním.

6. K zaúčtování řádků deníku klikněte na možnost **Zaúčtovat deníky**.

7. Po zaúčtování deníků spotřeby je možné aktualizovat stav životního cyklu pracovního příkazu. Chcete-li například označit, že byl pracovní příkaz dokončen, můžete stav životního cyklu aktualizovat na hodnotu ukončeno.

    - V poli **Zobrazit** v horní části stránky **Deníky pracovních příkazů** vyberte řádky deníku, které chcete zobrazit: **všechny**, **nezaúčtované** nebo **zaúčtované**. Zaúčtované deníky mají zaškrtnutí v poli **Zaúčtováno**.  
    - Při vytvoření řádků položek v deníku pracovních příkazů se dimenze produktu a sledovací dimenze související s danou položkou automaticky přesunou do řádku deníku.  

Snímek obrazovky níže ukazuje příklad registrace hodin a položek na pracovním příkazu v **Denících pracovních příkazů**.

![Obrázek č. 1](media/01-consumption.png)


## <a name="split-hours-on-work-orders-with-several-work-order-jobs"></a>Rozdělit hodiny na pracovní objednávky s několika úlohami pracovních příkazů

Obsahuje-li pracovní příkaz několik úloh pracovního příkazu, můžete zaregistrovat pracovní dobu pomocí funkce **Rozdělení hodin**, což znamená, že jeden řádek registrace hodin lze rovnoměrně rozložit na každé úloze pracovního příkazu.

1. Klikněte na **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.

2. Vyberte pracovní příkaz a klikněte na položku **Deníky**.

3. Vyberte řádek registrace hodin, který chcete rozdělit, a klepněte na možnost **Rozdělení hodin**.

4. V dialogovém okně **Rozdělení hodin v práci údržby prac. příkazu** je v poli **Pracovník** automaticky zobrazen název přihlášeného pracovníka. V případě potřeby můžete vybrat jiného pracovníka.

5. V poli **Kategorie** vyberte kategorii pro registraci hodin.

6. Zadejte počet odpracovaných hodin, které mají být rozděleny v poli **Hodiny**.

    ![Obrázek č. 2](media/02-consumption.png)

7. Klikněte na tlačítko **OK**.

*Příklad:* v dolní části obrazovky se zobrazí řádky deníku pro pracovní příkaz, které obsahují tři úlohy pracovního příkazu. První řádek, který obsahuje tři pracovní hodiny, byl rozdělen a pro každou úlohu pracovního příkazu je registrována jedna pracovní hodina. Po vytvoření tří řádků pro registraci hodin se rozhodnete, co dělat s původním řádkem registrace hodin (první řádek v příkladu). Můžete ji ponechat tak, jak je, nebo ji odstranit. 

![Obrázek č. 3](media/03-consumption.png)

## <a name="financial-dimensions-on-consumption-registrations"></a>Finanční dimenze pro registrace spotřeby

Při provádění registrace spotřeby se do registrací v určitém pořadí přidají finanční dimenze související s různými typy registrací. 

- *Registrace hodin a výdajů:* nejprve se přidají finanční dimenze ze záhlaví deníku, pokud existují. Dále se přidají finanční dimenze z souvisejícího projektu pracovního příkazu. Nakonec se přidají finanční dimenze od zdroje (pracovník).

- *Registrace položek:* nejprve se přidají finanční dimenze ze záhlaví deníku, pokud existují. Potom se přidají finanční dimenze z souvisejícího projektu pracovního příkazu. Dále budou přidány finanční dimenze z pracoviště. Nakonec se přidají finanční dimenze z položky.

>[!NOTE]
>Pro všechny tři typy registrace je ověřována kombinace finančních dimenzí a neplatné kombinace jsou prázdné. Jedná se o standardní nastavení v ostatních aplikacích Finance and Operations.

