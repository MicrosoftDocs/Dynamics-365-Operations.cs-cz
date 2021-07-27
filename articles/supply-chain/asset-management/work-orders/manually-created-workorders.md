---
title: Ručně vytvořené pracovní příkazy
description: Toto téma vysvětluje, jak vytvořit pracovní příkazy ručně v modulu Správa majetku.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderTableCreateRelated, EntAssetWorkOrderTableCreate, EntAssetWorkOrderTableCopy
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6e16c0bcd9521f822d0f92681e2a545439b78acb
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6354850"
---
# <a name="manually-created-work-orders"></a>Ručně vytvořené pracovní příkazy

[!include [banner](../../includes/banner.md)]


Pracovní příkazy lze vytvořit ručně dvěma způsoby:

- Na stránce **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy** 
- Ze stránky **Všechny požadavky na údržbu** nebo **Aktivní požadavky na údržbu** nebo **Požadavky na údržbu v mém funkčním místě**. 

## <a name="create-work-order"></a>Vytvořit pracovní příkaz

1. Vyberte **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.

2. Zvolte **Nové**.

3. V dialogovém okně **Vytvořit pracovní příkaz** vyberte typ pracovního příkazu v poli **Typ pracovního příkazu**.

4. Pokud je to nutné, vyberte **popis**.

5. V poli **Majetek** vyberte majetek.

>[!NOTE]
>Vyberete-li majetek, mohou být v rozevíracím seznamu **Majetek** k dispozici tři karty: 

- **Aktivní majetek** - obsahuje seznam všech datových zdrojů, které jsou aktivní pro stav životnosti majetku. 
- **Zobrazení majetku** - zobrazuje stromové zobrazení funkčních míst a datových zdrojů nainstalovaných v těchto umístěních.
- **Můj majetek** – Tato karta obsahuje majetek související s funkčními místy, ke kterým může být přiřazen (pracovník, který je přihlášený do systému). (Informace o nastavení naleznete v tématu [Pracovníci údržby a skupiny pracovníků](../setup-for-objects/workers-and-worker-groups.md).) Pokud pro pracovníka nejsou nastavena žádná funkční místa v části [Pracovníci údržby a skupiny pracovníků](../setup-for-objects/workers-and-worker-groups.md), karta **Můj majetek** není dostupná. 

6. V poli **Typ práce údržby** vyberte typ práce údržby pro pracovní příkaz.

7. V případě potřeby vyberte **Varianta typu práce údržby** a **Obchod**.

8. V případě potřeby lze úroveň služeb pracovního příkazu v poli **Úroveň služeb** změnit.

9. V příslušných polích vyberte **Očekávané počáteční** a **očekávané koncové** datum.

10. Kliknutím na **OK** vytvořte pracovní příkaz.

11. Na stránce se seznamem **Všechny pracovní příkazy** můžete podle potřeby upravit požadovaný pracovní příkaz.

Mějte na paměti následující body:

- V podrobném zobrazení na stránce **Všechny pracovní příkazy** můžete přidat několik majetků do pracovního příkazu v zobrazení Podrobností přidáním řádků na pevné záložce **Práce údržby pracovního příkazu**. U majetku můžete vybrat pouze typy prací údržby, které jsou definovány v typu majetku vybraném pro daný majetek.  

- Změníte-li v tomto nastavení kritičnost majetku poté, co jste jej již použili v pracovním příkazu, nebude tato servisní úroveň kritičnost v pracovním příkazu odpovídajícím způsobem aktualizována. Další informace o úrovních servisu a závažností naleznete v tématu [Úrovně servisu majetku](../setup-for-objects/object-priorities.md) a [Typy závažností majetku](../setup-for-objects/object-criticalities.md).

- Závažnost v pracovním příkazu je přepočítána pokaždé, když je v pracovním příkazu přidán nebo odstraněn řádek.

- V podrobném zobrazení **Všechny pracovní příkazy** > karta **Záhlaví** > pevná záložka **Plán** ve skupině **Zodpovědná osoba** nebo v poli **Zodopovědná osoba** můžete vybrat skupinu odpovědného pracovníka údržby nebo odpovědného pracovníka údržby. Tato nastavení lze změnit, pokud je pracovní příkaz aktivní. Lze je například změnit, když se změní stav životního cyklu pracovního příkazu. Automatický výběr provedený při vytvoření pracovního příkazu je založen na nastavení na stránce **Odpovědní pracovníci údržby**. Pokud přidáte nebo odeberete úlohy pracovní objednávky po vytvoření pracovní objednávky a pole **Odpovědná skupina** a pole **Odpovědný** jsou při aktualizaci pracovního příkazu prázdné, vyhledá Správa majetku možné párování ve formuláři nastavení pro skupinu odpovědných pracovníků údržby nebo odpovědného pracovníka údržby pro možnou shodu na stránce nastavení. Pokud je pole **Odpovědná skupina** nebo **Odpovědný pracovník** po aktualizaci pracovního příkazu už nastaveno, nebudou provedeny žádné změny. Další informace o tom, jak nastavit zodpovědné pracovníky pdržby a skupiny pracovníků, naleznete v tématu [Zodpovědní pracovníci údržby](../setup-for-maintenance-requests/responsible-workers.md).

- Ze stránky [Stav údržby](../controlling-and-reporting/maintenance-status.md) můžete provést výpočet pro získání přehledu pracovního vytížení, které se týkají příchozích a dokončených pracovních příkazů.  

- V zobrazení podrobností na stránce **Všechny pracovní příkazy** na pevné záložce **Podrobnosti řádku** můžete pomocí polí **Zeměpisná šířka** a **Zeměpisná délka** přidat zeměpisné souřadnice majetku vybraného v úloze pracovního příkazu.  


## <a name="create-related-work-order"></a>Vytvořit související pracovní příkaz

Můžete vytvořit pracovní příkaz na základě stávajícího pracovního příkazu. To je užitečné třeba v případě, že chcete registrovat primární a sekundární pracovní příkazy. Nový pracovní příkaz je založen na úloze pracovního příkazu z existujícího pracovního příkazu.

1. Vyberte **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.

2. Vyberte pracovní příkaz, pro který chcete vytvořit související pracovní příkaz.

3. V podokně akcí na kartě **Pracovní příkaz** ve skupině **Nový** vyberte **Související pracovní příkaz**.

4. V dialogovém okně **Vytvořit související pracovní příkaz** vyberte úlohu pracovního příkazu, pro kterou chcete vytvořit související pracovní příkaz v poli **Úloha pracovního příkazu**.

5. V poli **Typ práce údržby** vyberte typ práce údržby.

6. V polích **Varianta typu práce údržby** a **Obor** vyberte pro typ práce údržby související variantu typu práce údržby a obor.

7. Je-li tento pracovní příkaz první související pracovní příkaz, který byl vytvořen pro vybraný pracovní příkaz, postupujte takto:
    1. Vyberte možnost **Nový pracovní příkaz**.
    2. V poli **Typ pracovního příkazu** vyberte typ pracovního příkazu.
    3. Zadejte popis do pole **Popis**.
    4. V případě potřeby změňte úroveň služeb pracovního příkazu v poli **Úroveň služeb**.
    5. V polích **Očekávaný začátek** a **Očekávaný konec** vyberte počáteční a koncové datum.
    6. Vyberte **OK**. Nový související pracovní příkaz se zobrazí na stránce seznamu **Všechny pracovní příkazy**.  

8. Pokud se jedná o pracovní příkaz, pro který vytváříte tent související pracovní příkaz, pro již existují související pracovní příkazy, přidejte pomocí následujících kroků novou úlohu pracovního příkazu do existujícího souvisejícího pracovního příkazu:
    1. Vyberte možnost **Přidat do souvisejícího pracovního příkazu**.
    2. Pak v poli **pracovní příkaz** vyberte související pracovní příkaz, ke kterému chcete přidat novou úlohu pracovního příkazu.
    3. V případě potřeby změňte úroveň služeb pracovního příkazu v poli **Úroveň služeb**.
    4. V polích **Očekávaný začátek** a **Očekávaný konec** změňte podle potřeby očekávané počáteční a koncové datum.
    5. Vyberte **OK**. Úloha pracovního příkazu se přidá do existujícího souvisejícího pracovního příkazu.

Na následujícím obrázku je uveden příklad dialogu **Vytvořit související pracovní příkaz**.

![Obrázek č. 1.](media/03-work-orders.png)

>[!NOTE]
>Pokud jste nastavili související masku pracovního příkazu na kartě **Parametry správy majetku** > **Pracovní příkazy** > **Související maska pracovního příkazu**, budou v souladu s nastavením masky vytvořena ID pracovních příkazů. Není-li nastavena žádná související maska pracovního příkazu, bude pro související pracovní příkazy použito další dostupné ID pracovního příkazu.

## <a name="copy-a-work-order"></a>Zkopírování pracovního příkazu

Nový pracovní příkaz lze rychle vytvořit z existujícího pracovního příkazu. Tento postup práce s pracovními příkazy se liší od vytváření pracovních příkazů na základě [plánů údržby](../preventive-and-reactive-maintenance/maintenance-plans.md). To je užitečné například v případě, že máte pracovní příkaz obsahující mnoho úloh pracovního příkazu s různými úlohami v různých majetcích, které by měly být v pravidelných intervalech dokončeny.

1. Vyberte **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.

2. Vyberte pracovní příkaz, ze kterého chcete kopírovat obsah.

3. V podokně akcí na kartě > **Pracovní příkaz** ve skupině > **Nový** vyberte **Kopírovat pracovní příkaz**.

4. Zobrazí se nastavení pracovního příkazu z vybraného pracovního příkazu. V případě potřeby můžete některá pole upravit.

5. Výběrem **OK** vytvořte nový pracovní příkaz.

6. Na stránce se seznamem **Všechny pracovní příkazy** můžete podle potřeby upravit požadovaný pracovní příkaz.

>[!NOTE]
>Při vytvoření nového pracovního příkazu se některé informace zkopírují přímo z existujícího pracovního příkazu. Informace o prognózách, nástrojích, kontrolních seznamech údržby, funkčním místě, adresách a plánování nejsou kopírovány. Místo toho je inicializován z aktuálního nastavení v modulu Správa majetku. Proto, pokud byly tyto informace změněny mezi časem vytvoření prvního pracovního příkazu a časem, kdy jste provedli kopii pracovní objednávky, budou změny zahrnuty do nového pracovního příkazu. Příkladem jsou změny v prognózách nebo aktualizace kontrolních seznamů údržby.

Na následujícím obrázku je uveden příklad dialogového okna **Kopírovat pracovní příkaz**.

![Obrázek č. 2.](media/04-work-orders.png)


## <a name="create-a-work-order-based-on-a-maintenance-request"></a>Vytvoření pracovního příkazu na základě požadavku na údržbu

1. Vyberte **Správa majetku** > **Společné** > **Požadavky na údržbu** > **Všechny požadavky na údržbu** nebo **Aktivní požadavky na údržbu**.

2. Vyberte požadavek na údržbu, pro který chcete vytvořit pracovní příkaz, a klikněte na tlačítko **Upravit**.

3. V podokně akcí na kartě > **Požadavek na údržbu** ve skupině > **Nový** vyberte **Pracovní příkaz**.

4. V dialogovém okně **Pracovní příkaz** nastavte pole. Pokud byl v požadavku na údržbu vybrán typ úlohy údržby, můžete v případě potřeby vybrat jiný typ úlohy údržby při vytvoření pracovního příkazu.

5. Vyberte **OK**. Zpráva vás informuje o tom, že byl pracovní příkaz vytvořen.

6. Chcete-li zobrazit, které pracovní příkazy jsou spojeny s požadavkem na údržbu, vyberte požadavek na údržbu v seznamech **Všechny požadavky na údržbu** nebo **Aktivní požadavky na údržbu** a klikněte na tlačítko Pracovní příkazy. Pak v podokně akcí na kartě **Požadavek na údržbu** ve skupině **Zobrazit** vyberte **Pracovní příkazy**.


Na následujícím obrázku je uveden příklad dialogového okna **Vytvořit pracovní příkaz**.

![Obrázek č. 3.](media/05-work-orders.png)


>[!NOTE]
>Pokud chcete, aby se pracovní příkazy vytvářely automaticky, můžete naplánovat úlohy plánu údržby nebo nastavit automatické vytvoření [plánů údržby](../preventive-and-reactive-maintenance/maintenance-plans.md) nebo [pořadí údržby](../preventive-and-reactive-maintenance/maintenance-rounds.md) u majetku. Pracovní příkazy vytvořené z požadavků na údržbu na stránce se seznamem **Rozvrh veškeré údržby** jsou vytvořeny s typy úloh údržby vybranými v požadavcích na údržbu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]