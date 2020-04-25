---
title: Kontrolní seznamy údržby
description: Tohle téma popisuje kontrolní seznamy údržby v modulu Správa majetku.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5a9973840021bd49c0878ab9252bbba9161fd283
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208148"
---
# <a name="maintenance-checklists"></a>Kontrolní seznamy údržby

[!include [banner](../../includes/banner.md)]



Kontrolní seznamy údržby se nastavují pro typy práce údržby. Vyplnění kontrolních seznamů údržby je součástí procesu tvorby pracovního příkazu. Další informace o vytvoření kontrolních seznamů údržby v typech práce údržby naleznete v části **kategorie typů práce údržby, typy práce údržby , varianty typů práce údržby, obory práce údržby a kontrolní seznamy údržby** ve formuláři [Výchozí hodnoty typu práce údržby](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).

Při práci s kontrolními seznamy údržby v rámci pracovního příkazu můžete vyplnit předdefinované kontrolní seznamy údržby, které souvisejí s typy práce údržby. Dále je možné přidat další kontrolní seznamy údržby.


## <a name="fill-in-a-maintenance-checklist"></a>Vyplnění kontrolního seznamu údržby

1. Klikněte na **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.

2. Vyberte pracovní příkaz v seznamu a pak v podokně akcí na kartě **Pracovní příkaz** ve skupině **Řádky** vyberte **Kontrolní seznam údržby**.

3. V **kontrolním seznamu práce údržby pracovního příkazu** se nacházejí kontrolní seznamy údržby pro všechny úlohy pracovních příkazů. Pokud mají úlohy pracovních příkazů různé typy práce údržby, mohou se u každé úlohy pracovních příkazů lišit. Vyberte úlohu pracovního příkazu pro práci se souvisejícím kontrolním seznamem údržby. Podrobnosti o vybraném řádku kontrolního seznamu údržby jsou zobrazeny na záložce s náhledem **Podrobnosti řádku**.

4. Postupně dokončete všechny řádky kontrolního seznamu údržby, a to v pořadí, v jakém jsou zobrazeny. Řádek kontrolního seznamu údržby zadáte vyplněním polí na záložce s náhledem **Podrobnosti řádku**. Informace, které jsou nutné k dokončení řádku, se mohou lišit v závislosti na typu řádku. Například na řádku typu **Text** přidáte poznámku vysvětlující, co bylo výsledkem kontroly. Na řádku typu **Měření** zadáte hodnotu čítače, kterou načtete na zařízení, a v případě potřeby také můžete přidat poznámku. Řádek kontrolního seznamu údržby typu **Záhlaví** se používá jako záhlaví kvůli seskupení řádků kontrolního seznamu údržby pod ním. Není nutné vyplnit záhlaví. Jako u všech ostatních typů řádků kontrolního seznamu údržby můžete přidat poznámku k řádku typu **záhlaví**.

5. Pokud pokyny souvisejí s řádkem kontrolního seznamu údržby, je zaškrtnuto políčko **Pokyny**. Přečtěte si pokyny pro vybraný řádek kontrolního seznamu údržby v poli **Pokyny** na pevné záložce **Podrobnosti řádku**.

6. Po vytvoření řádku kontrolního seznamu údržby zaškrtněte na řádku políčko **Zkontrolováno**, které chcete označit jako dokončené. Chcete-li zrušit řádek kontrolního seznamu údržby, protože není relevantní pro úlohu pracovního příkazu, zaškrtněte políčko **Není k dispozici** v řádku. Pokud je zaškrtnuto políčko **Povinné** na řádku kontrolního seznamu údržby, musíte vybrat políčko **Zkontrolováno** nebo **N/A**.

>[!NOTE]
>Registrace kontrolního seznamu údržby lze aktualizovat pouze v případě, že je v [aktivním](../setup-for-work-orders/work-order-lifecycle-states.md) stavu životního cyklu.  


## <a name="add-a-maintenance-checklist-line"></a>Přidání řádku kontrolního seznamu údržby

Kontrolní seznamy údržby jsou vytvářeny z definice výchozího typu práce údržby a jsou převedeny na úlohu pracovního příkazu. V případě potřeby můžete přidat řádky kontrolního seznamu údržby do úlohy pracovního příkazu. Ručně přidané řádky kontrolního seznamu údržby získají odkaz **Ruční**.

1. Na stránce **Kontrolní seznam práce údržby pracovního příkazu** vyberte úlohu pracovního příkazu, které chcete přidat do kontrolního seznamu údržby.

2. Na pevné kartě **Řádky kontrolního seznamu údržby** vyberte řádek kontrolního seznamu údržby. Chcete-li vložit nový řádek za vybraný řádek, stiskněte klávesu s **šipkou dolů**. Další číslo v pořadí je automaticky zadáno do pole **Číslo řádku**. Chcete-li vložit nový řádek před vybraný řádek, vyberte možnost **Přidat řádek**. 

3. Do pole **Název** zadejte název řídku kontrolního seznamu údržby.

4. V poli **Typ** vyberte typ řádku kontrolního seznamu údržby. Na pevné záložce **Podrobnosti řádku** jsou pro každý typ kontrolního seznamu údržby zobrazeny související pole.
    - **Text** - tento typ slouží k přidání řádku kontrolního seznamu údržby s textem, který popisuje, co je nutné provést. Tento typ kontrolního seznamu údržby můžete například použít v případě, že chcete, aby pracovník mohl zkontrolovat nebo prohlédnout nějaký objekt, ale neočekáváte určitý (měřitelný) výsledek. Po výběru tohoto typu na pevné záložce **Podrobnosti řádků** v poli **Pokyny** zadejte text popisující, co je třeba provést.
    - **Záhlaví** - řádek kontrolního seznamu údržby tohoto typu se používá jako záhlaví kvůli seskupení řádků kontrolního seznamu údržby pod ním. Tento typ je užitečný v případě, že máte několik řádků kontrolního seznamu údržby, které lze rozdělit na určité oblasti. Po výběru tohoto typu zadejte do pole **Název** jeho popisný název.
    - **Šablona** - Tento typ nelze použít, pokud do úlohy pracovního příkazu ručně přidáte řádek kontrolního seznamu údržby ručně.  
    - **Proměnná** - Tento typ slouží k definování možného výsledku v rozsahu na řádku kontrolního seznamu údržby. Informace o nastavení proměnných kontrolního seznamu údržby jsou popsány v tématu [Kategorie typů práce údržby, typy práce údržby , varianty typů práce údržby, obory práce údržby a kontrolní seznamy údržby](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md) Po výběru tohoto typu zadejte do pole **Název** popisný název proměnné. Na pevné záložce **Podrobnosti řádku** v poli **Proměnná** vyberte proměnnou. V poli **Pokyny** zadejte popis toho, co má být provedeno.
    - **Měření** – tento typ slouží k zaznamenání konkrétních měření do řádku kontrolního seznamu údržby. Po výběru tohoto typu zadejte do pole **Název** název měření. Na pevné záložce **Podrobnosti řádku** vyberte příslušné hodnoty v poli **Čítač** a **Jednotka**. V poli **Pokyny** zadejte popis toho, co má být provedeno.

5. Po ručním přidání řádků kontrolního seznamu údržby vplňte řádky podle popisu v části **Vyplnění kontrolního seznamu údržby** nahoře.

>[!NOTE]
>Na stránce **Kontrolní seznam úloh údržby pracovního příkazu** nelze odstranit řádky kontrolního seznamu údržby s referencí **Typ úlohy**. Odstranit lze pouze řádky kontrolního seznamu údržby s odkazem **Ruční**, které jste ručně vytvořili vy nebo jiní pracovníci údržby.

Následující ilustrace znázorňuje příklad kontrolního seznamu údržby.

![Obrázek č. 1](media/14-work-orders.png)

