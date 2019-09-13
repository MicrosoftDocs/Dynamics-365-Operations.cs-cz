---
title: Kontrolní seznamy údržby
description: Tohle téma popisuje kontrolní seznamy údržby v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 325ff1fa0811d6aac5189cc69f21483fce6b3e8f
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875552"
---
# <a name="maintenance-checklists"></a>Kontrolní seznamy údržby


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Kontrolní seznamy údržby se nastavují pro typy práce údržby a používají se při práci s pracovními příkazy. Vyplnění kontrolních seznamů údržby je součástí tvorby pracovního příkazu. Další informace o vytvoření kontrolních seznamů údržby v typech práce údržby naleznete v části [kategorie typů práce údržby, typy práce údržby , varianty typů práce údržby, obory práce údržby a kontrolní seznamy údržby](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md) ve formuláři **Výchozí hodnoty typu práce údržby**.

Při práci s kontrolními seznamy údržby v rámci pracovního příkazu můžete vyplnit předdefinované kontrolní seznamy údržby, které souvisejí s typy práce údržby. Dále je možné přidat další kontrolní seznamy údržby.

## <a name="fill-out-a-maintenance-checklist"></a>Vyplnění kontrolního seznamu údržby

1. Klikněte na **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.

2. Vyberte pracovní příkaz a klikněte na položku **Kontrolní seznam údržby**.

3. V **kontrolním seznamu práce údržby pracovního příkazu** se nachází kontrolní seznamy údržby pro všechny úlohy pracovních příkazů. Pokud mají úlohy pracovních příkazů různé typy práce údržby, mohou se u každé úlohy pracovních příkazů lišit. Vyberte úlohu pracovního příkazu pro práci se souvisejícím kontrolním seznamem údržby. Podrobnosti o vybraném řádku kontrolního seznamu údržby jsou zobrazeny na záložce s náhledem **Podrobnosti řádku**.

4. Postupně dokončete všechny řádky kontrolního seznamu údržby, a to v pořadí, v jakém jsou zobrazeny. Řádek kontrolního seznamu údržby typu „Záhlaví“ se používá jako záhlaví kvůli seskupení řádků kontrolního seznamu údržby pod ním. Není nutné vyplnit záhlaví, ale jako u všech typů řádků kontrolního seznamu údržby lze do záhlaví přidat **poznámku**.

5. Pokud pokyny souvisejí s řádkem kontrolního seznamu údržby, je zaškrtnuto políčko **Pokyny**. Přečtěte si pokyny pro vybraný řádek kontrolního seznamu na záložce s náhledem údržby na záložce s náhledem **Podrobnosti řádku** > v sekci **Pokyny**.

6. Informace potřebné k dokončení řádku kontrolního seznamu údržby se mohou lišit v závislosti na typu kontrolního seznamu údržby. Řádek kontrolního seznamu údržby zadáte vyplněním polí na záložce s náhledem **Podrobnosti řádku**. Například na řádku typu text přidáte **poznámku** vysvětlující, co bylo výsledkem tohoto řádku kontrolního seznamu. V řádku typu měření přidejte **hodnotu čítače**, kterou načtete na zařízení, a v případě potřeby také můžete přidat **poznámku**.

- Po vytvoření řádku kontrolního seznamu údržby zaškrtněte na řádku políčko **Zkontrolováno**, které chcete označit jako dokončené. Chcete-li zrušit řádek kontrolního seznamu údržby, protože není relevantní pro úlohu pracovního příkazu, zaškrtněte políčko **Není k dispozici** v řádku. Je-li řádek kontrolního seznamu údržbyoznačen jako **Povinný**, je nutné jej označit jako "Zkontrolováno", nebo "Není k dispozici".  
- Registrace kontrolního seznamu údržby lze aktualizovat pouze v případě, že je v [aktivním](../setup-for-work-orders/work-order-lifecycle-states.md) stavu životního cyklu.  


## <a name="add-a-maintenance-checklist-line"></a>Přidání řádku kontrolního seznamu údržby

Kontrolní seznamy údržby jsou vytvářeny z definice výchozího typu práce údržby a jsou převedeny na úlohu pracovního příkazu. V případě potřeby můžete přidat řádky kontrolního seznamu údržby do úlohy pracovního příkazu. Ručně přidané řádky kontrolního seznamu údržby získají odkaz "Ruční".

1. V **kontrolním seznamu práce údržby pracovního příkazu** vyberte úlohu pracovního příkazu, které chcete přidat do kontrolního seznamu údržby.

2. Na záložce náhledu **Řádky kontrolního seznamu údržby** vyberte řádek kontrolního seznamu údržby a stiskněte tlačítko se šipkou dolů, pokud chcete vložit nový řádek za řádek kontrolního seznamu údržby. Další číslo v pořadí je automaticky vloženo do pole **Číslo řádku**. Můžete také vybrat řádek kontrolního seznamu údržby a kliknutím na tlačítko **Přidat řádek** vložit nový řádek nad vybraný řádek kontrolního seznamu údržby.

3. Do pole **Název** zadejte název řídku kontrolního seznamu údržby.

4. V poli **Typ** vyberte typ řádku kontrolního seznamu údržby. Na záložce s náhledem **Podrobnosti řádku** jsou pro každý typ kontrolního seznamu údržby zobrazeny související pole.  
  a. Položka „text“ slouží k přidání řádku kontrolního seznamu údržby s textovým popisem postupu. Tento typ kontrolního seznamu údržby použijte v případě, že chcete, aby pracovník mohl zkontrolovat nebo prohlédnout nějaký objekt, ale neočekáváte určitý (měřitelný) výsledek. Zadejte popis toho, co dělat, v části **Pokyny** na záložce s náhledem **Podrobnosti řádku**. b. „Záhlaví“ se používá jako záhlaví kvůli seskupení řádků kontrolního seznamu údržby, který se zobrazí pod ním. To je užitečné v případě, že máte několik řádků kontrolního seznamu údržby, které lze rozdělit na určité oblasti. Do pole **Název** zadejte popisný název.  
  c. Položku „Šablona“ nelze použít, pokud do úlohy pracovního příkazu přidáte řádek kontrolního seznamu údržby ručně.  
  d Položka „proměnná“ slouží k definování možného výsledku v rozsahu na řádku kontrolního seznamu údržby. Nastavení proměnných kontrolního seznamu údržby je popsáno v tématu [Kategorie typů práce údržby, typy práce údržby , varianty typů práce údržby, obory práce údržby a kontrolní seznamy údržby](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md) Do pole **Název** zadejte název popisující proměnnou. V poli **Proměnná** zvolte proměnnou. Zadejte popis toho, co dělat, v části **Pokyny** na záložce s náhledem **Podrobnosti řádku**.  
  e. „Měření“ slouží k zaznamenání určitého měření. Do pole **Název** zadejte název měření. Na záložce s náhledem **Podrobnosti řádku** vyberte **Čítač** a **Jednotka**. Zadejte popis toho, co dělat, v části **Pokyny**.  

5. Po ručním přidání řádků kontrolního seznamu údržby vyplňte řádky podle pokynů v předchozí části.

>[!NOTE]
>V **kontrolním seznamuúlohy údržby pracovního příkazu** nelze odstranit řádky kontrolního seznamu údržby s odkazem „Typ práce“. Odstranit lze pouze řádky kontrolního seznamu údržby s odkazem "Ruční", které jste ručně vytvořili vy nebo jiní pracovníci údržby.


![Obrázek č. 1](media/14-work-orders.png)

