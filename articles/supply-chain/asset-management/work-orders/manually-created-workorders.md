---
title: Ručně vytvořené pracovní příkazy
description: Toto téma vysvětluje, jak vytvořit pracovní příkazy ručně v modulu Správa majetku.
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
ms.openlocfilehash: 261448a134a7c1aacfbb4ea6f954ce03a63c23e2
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875545"
---
# <a name="manually-created-work-orders"></a>Ručně vytvořené pracovní příkazy

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Pracovní příkazy lze vytvořit ručně dvěma způsoby:

- ve **Všech pracovních příkazech** nebo **Aktivních pracovních příkazech**  
- ve **Všech požadavcích na údržbu** nebo **Aktivních požadavcích na údržbu** nebo **Požadavcích na údržbu v mém funkčním místě**  

## <a name="create-work-order"></a>Vytvořit pracovní příkaz

1. Klikněte na **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.

2. Klikněte na tlačítko **Nový**.

3. V rozevíracím seznamu **Vytvořit pracovní příkaz** vyberte typ pracovního příkazu.

4. Pokud je to nutné, vyberte popis.

5. Vyberte majetek pro pracovní příkaz a typ práce údržby.

>[!NOTE]
>Když vyberete majetek, jsou k dispozici tři karty: karta **Můj majetek** obsahuje majetek související s funkčními místy, do kterých můžete být přidělení (pracovník údržby, který je přihlášen k systému) (nastavení v [Pracovníci údržby a skupiny pracovníků](../setup-for-objects/workers-and-worker-groups.md)). Nejsou-li u pracovníka údržby ve formuláři [Pracovníci údržby a skupiny pracovníků](../setup-for-objects/workers-and-worker-groups.md) nastavena žádná funkční umístění, nebude karta **můj majetek** viditelná. Karta **Aktivní majetek** obsahuje seznam všech datových zdrojů, které jsou aktivní pro stav životnosti majetku. Karta **Zobrazení majetku** zobrazuje stromové zobrazení funkčních míst a datových zdrojů nainstalovaných v těchto umístěních.

6. V případě potřeby vyberte **Varianta typu práce údržby** a **Obchod**.

7. V případě potřeby lze úroveň služeb pracovního příkazu v poli **Úroveň služeb** změnit.

8. V souvisejících polích vyberte očekávaná počáteční a koncová data.

9. Klepnutím na **OK** vytvořte nový pracovní příkaz.

10. Upravte pracovní příkaz ve **Všech pracovních příkazech**, je-li to vyžadováno.

- Ve **Všech pracovních příkazech** můžete přidat několik majetků do pracovního příkazu v zobrazení Podrobností přidáním řádků na pevné záložce **Práce údržby pracovního příkazu**. U majetku můžete vybrat pouze typy prací údržby, které jsou definovány v typu majetku vybraném pro daný majetek.  
- Pokud jste změnili úroveň služby Majetek nebo kritičnost majetku po jejich použití v pracovním příkazu (viz informace [Úrovně služby Majetek](../setup-for-objects/object-priorities.md) a [Kritičnosti majetku](../setup-for-objects/object-criticalities.md)), nebude se úroveň služeb nebo kritičnost v pracovním příkazu odpovídajícím způsobem aktualizovat.
- Kritičnost na pracovním příkazu je přepočítána pokaždé, když je v pracovním příkazu přidán nebo odstraněn řádek.
- V zobrazení podrobností **Všechny pracovní příkazy** > zobrazení **Záhlaví** > pevné záložce **Plán** můžete vybrat skupinu odpovědného pracovníka údržby nebo odpovědného pracovníka údržby v poli **Odpovědná skupina** nebo **Odpovědný**. Toto nastavení lze změnit, pokud je pracovní příkaz aktivní, například při změně stavu životního cyklu pracovního příkazu. Automatický výběr provedený při vytvoření pracovního příkazu je založen na nastavení v položce **Odpovědní pracovníci údržby**. Pokud přidáte nebo odeberete úlohy pracovní objednávky po vytvoření pracovní objednávky a pole **Odpovědná skupina** a pole **Odpovědný** jsou při aktualizaci pracovního příkazu prázdné, vyhledá Správa majetku možné párování ve formuláři nastavení pro skupinu odpovědných pracovníků údržby nebo odpovědného pracovníka údržby. Pokud je pole **Odpovědná skupina** nebo **Odpovědný** po aktualizaci pracovního příkazu vyplněno, nebudou provedeny žádné změny. 

- Ve **Stavu údržby** můžete provést výpočet pro získání přehledu pracovního vytížení, které se týkají příchozích a dokončených pracovních příkazů.  

- Na pevné záložce **Podrobnosti řádku** použijte pole **Zeměpisná šířka** a **Zeměpisná délka** k přidání geografických souřadnic pro majetek vybraný na pracovním příkazu.  

## <a name="create-related-work-order"></a>Vytvořit související pracovní příkaz

Související pracovní příkaz můžete vytvořit pro existující pracovní příkaz, pokud například chcete pracovat s primárními a sekundárními pracovními příkazy. Nový pracovní příkaz je založen na úloze pracovního příkazu z existujícího pracovního příkazu.

1. Klikněte na **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.

2. Vyberte pracovní příkaz, pro který chcete vytvořit související pracovní příkaz.

3. Klikněte na **Související pracovní příkaz**.

4. V rozevíracím dialogovém okně **Vytvořit související pracovní příkaz** vyberte úlohu pracovního příkazu, pro kterou chcete vytvořit související pracovní příkaz v poli **Úloha pracovního příkazu**.

5. Vyberte typ úlohy údržby v poli **Typ úlohy údržby** a v případě potřeby i související variantu typu úlohy údržby a obchod v polích **Varianta typu práce údržby** a **Oobchod**.

6. Pokud se jedná o první související pracovní příkaz, klikněte na přepínač **Nový pracovní příkaz**.

7. V souvisejících polích vyberte **Typ pracovního příkazu** a **Popis**.

8. V případě potřeby změňte úroveň služeb pracovního příkazu v poli **Úroveň služeb**.

9. Vložte očekávaná počáteční a koncová data v souvisejících polích.

10. Klikněte na tlačítko **OK**. Nový související pracovní příkaz se zobrazí v seznamu **Všechny pracovní příkazy**.

11. Pokud vytvoříte související pracovní příkaz na pracovním příkazu, který již obsahuje související pracovní příkazy, můžete úlohu pracovního příkazu přidat do již souvisejícího pracovního příkazu. To lze provést kliknutím na přepínač **Přidat k souvisejícímu pracovnímu příkazu** v kroku 6. Poté vyberte související pracovní příkaz, ke kterému chcete přidat novou úlohu pracovního příkazu. Podle potřeby upravte pole **Úroveň služeb**, **Očekávané zahájení** a **Očekávaný konec** a klikněte na tlačítko **OK**. Úloha pracovního příkazu se přidá do existujícího souvisejícího pracovního příkazu.


![Obrázek č. 1](media/03-work-orders.png)

**Poznámka:** Pokud jste nastavili související masku pracovního příkazu v **Parametry správy majetku** > **Pracovní příkazy** > **Související maska pracovního příkazu**, budou v souladu s nastavením masky vytvořeny ID pracovních příkazů. Není-li nastavena žádná související maska pracovního příkazu, bude pro související pracovní příkazy použito další dostupné ID pracovního příkazu.

## <a name="copy-work-order"></a>Zkopírovat pracovní příkaz

Nový pracovní příkaz lze rychle vytvořit z existujícího pracovního příkazu. Tento postup práce s pracovními příkazy se liší od vytváření pracovních příkazů na základě plánů údržby. To je užitečné například v případě, že máte pracovní příkaz obsahující mnoho úloh pracovního příkazu s různými úlohami v různých majetcích, které by měly být v pravidelných intervalech dokončeny.

1. Klikněte na **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.

2. Vyberte pracovní příkaz, ze kterého chcete kopírovat obsah.

3. Klikněte na **Kopírovat pracovní příkaz**. Zobrazí se nastavení pracovního příkazu z vybraného pracovního příkazu. V případě potřeby můžete některá pole upravit.

4. Klepnutím na **OK** vytvořte nový pracovní příkaz.

5. Upravte pracovní příkaz ve **Všech pracovních příkazech**, je-li to vyžadováno.

>[!NOTE]
>Při vytvoření nového pracovního příkazu se některé informace zkopírují přímo z existujícího pracovního příkazu. Informace týkající se prognóz, nástrojů, kontrolních seznamů údržby, funkčního umístění, adres a plánování nejsou zkopírovány, ale inicializovány z aktuálního nastavení v modulu Správa majetku. To znamená, že pokud byly změny provedeny v datech od vytvoření prvního pracovního příkazu až po dobu jeho kopie, budou tyto změny zahrnuty do nově vytvořeného pracovního příkazu. Příkladem jsou změny v prognózách nebo aktualizované kontrolní seznamy údržby.


![Obrázek č. 2](media/04-work-orders.png)


## <a name="create-work-order-based-on-a-maintenance-request"></a>Vytvoření pracovního příkazu na základě požadavku na údržbu

1. Klikněte na **Správa majetku** > **Společné** > **Požadavky na údržbu** > **Všechny požadavky na údržbu** nebo **Aktivní požadavky na údržbu**.

2. Vyberte požadavek na údržbu, pro který chcete vytvořit pracovní příkaz, a klikněte na tlačítko **Upravit**.

3. Ve **Všech požadavcích** klikněte na **Pracovní příkaz**.

4. Vyplňte rozevírací nabídku **Pracovní příkaz**. Pokud byl v požadavku na údržbu vybrán typ úlohy údržby, můžete v případě potřeby vybrat jiný typ úlohy údržby při vytvoření pracovního příkazu.

5. Klikněte na tlačítko **OK**. Zobrazí se zpráva s informacemi o tom, že byl vytvořen daný pracovní příkaz.

6. Chcete-li zobrazit, které pracovní příkazy jsou spojeny s požadavkem na údržbu, vyberte požadavek na údržbu v seznamech **Všechny požadavky na údržbu** nebo **Aktivní požadavky na údržbu** a klikněte na tlačítko **Pracovní příkazy**.


![Obrázek č. 3](media/05-work-orders.png)


>[!NOTE]
>Pracovní příkazy lze vytvářet také automaticky úlohami plánu údržby, nebo nastavením "automatického vytváření" plánů údržby nebo pořadí údržby majetku. Pracovní příkazy vytvořené z požadavků na údržbu v **Rozvrhu údržby** jsou vytvořeny s typy úloh údržby vybranými v požadavcích na údržbu.

