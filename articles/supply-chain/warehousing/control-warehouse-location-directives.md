---
title: Řízení práce ve skladu pomocí šablon práce a směrnic skladového místa
description: Toto téma popisuje způsob použití šablon práce a směrnic skladového místa k určení, jak a kde se práce ve skladu provádí.
author: perlynne
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocDirFailure, WHSLocDirHint, WHSLocDirTable, WHSLocDirTableUOM, WHSRFMenuItem, WHSWork, WHSWorkClass, WHSWorkPool, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72921
ms.assetid: 377ab8af-5b0c-4b5e-a387-06ac1e1820c0
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7e955fba12e963a443c0304f0a8a0e395c46909dd34de12cd51fa9788491786
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770137"
---
# <a name="control-warehouse-work-by-using-work-templates-and-location-directives"></a>Řízení práce ve skladu pomocí šablon práce a směrnic skladového místa

[!include [banner](../includes/banner.md)]

Toto téma popisuje způsob použití šablon práce a směrnic skladového místa k určení, jak a kde se práce ve skladu provádí.

Pokyny, které pracovníci skladu obdrží v mobilním zařízení, jsou určeny podle šablon práce, které nastavíte v aplikaci Dynamics 365 Supply Chain Management k definování různých procesů a úloh ve skladu. Šablony práce určují způsob provedení práce pro každý skladový proces. Přiřazením směrnic skladového místa k šablonám práce můžete pomoci zajistit, že práce bude probíhat v určitých fyzických oblastech skladu.

## <a name="work-templates"></a>Šablony práce

Stránka **Šablony práce** umožňují definovat pracovní operace, které musí být provedeny ve skladu. Obvykle pracovní operace ve skladu sestávají z páru akcí: skladoví pracovníci vyskladní zásoby na skladě na jednom místě a převedou vyskladněné zásoby v jiném skladovém místě. 

Šablony práce obsahují záhlaví a související řádky. Každá šablona práce je pro určitý *typ pořadí pracovních činností*. Mnohé typy pracovních činností jsou přidruženy ke zdrojovým dokumentům, jako je nákupní nebo prodejní objednávka. Ostatní typy pořadí pracovních činností však představují samostatné procesy skladu, jako je například cyklická inventura. *ID fondů práce* umožňuje uspořádat práci do skupin. 

Použijte nastavení v definici záhlaví práce k určení určit, kdy mají být vytvořeny nové části práce. Můžete například nastavit maximální počet řádků vyskladnění a maximální očekávaný čas vyskladnění. Poté pokud práce pro výdej prodejní objednávky překročí některé z těchto hodnot, práce je rozdělena do dvou pracovních částí.

Použijte tlačítko **Přerušení pracovního záhlaví** k určení, kdy má systém vytvořit nové pracovní hlavičky. Například k vytvoření pracovního záhlaví pro každé _číslo objednávky_ vyberte **Upravit dotaz** v podokně akcí a poté přidejte pole **Číslo objednávky** na kartu **Třídění** editoru dotazů. Pole přidaná na kartu **Třídění** jsou k dispozici pro výběr jako *seskupení polí*. Pokud chcete nastavit seskupení polí, vyberte v podokně akcí **Zalomení pracovních hlaviček** a u každého pole, které chcete použít jako seskupení, zaškrtněte políčko ve sloupci **Seskupit podle tohoto pole**.

Řádky práce představují fyzické úkoly, které jsou požadovány pro zpracování práce. Například pro proces výstupního skladu může existovat jeden řádek práce pro vyzvednutí položek v rámci skladu, a jeden řádek pro uložení těchto položek do přípravné oblasti. Poté může existovat další řádek pro výdej položek z fázování a jiný řádek pro vkládání položek do nákladního automobilu v rámci procesu nakládání. Podle potřeby můžete nastavit *kód předpisu* na řádcích šablony práce. Kód předpisu je propojen s předpisem pro skladové místo a proto pomáhá zaručit, že je skladová práce zpracována na správném místě ve skladu.

Můžete určit dotaz pro řízení toho, kdy dojde k použití určité šablony práce. Můžete například nastavit omezení, aby určitá šablona mohla být použita pouze pro určitý sklad. Případně můžete mít několik šablon, které se používají k vytvoření práce pro zpracování odchozí prodejní objednávky v závislosti na původu prodeje. Systém používá pole **Pořadové číslo** k určení pořadí, ve kterém jsou posuzovány šablony práce. Proto pokud máte velmi konkrétní dotaz na určitou šablonu práce, měli byste jí zadat nízké pořadové číslo. Tento dotaz bude poté vyhodnocen před ostatními obecnějšími dotazy.

> [!NOTE]
> Aby se zabránilo tomu, že systém automaticky přepíše *pořadová čísla* šablony práce po odstranění šablony, zapněte funkci *Zachovat pořadová čísla pracovních šablon při mazání* v okně [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Pokud chcete zastavit nebo pozastavit proces práce, můžete vybrat nastavení **Zastavit práci** na řádku práce. Pracovník, který provádí práci, v tomto případě nebude požádán o provedení dalšího kroku práce. Pokud se chcete přesunout na další krok, je třeba, aby tento nebo jiný pracovník práci znovu vybral. Můžete také oddělit úlohy v rámci práce pomocí jiného *ID třídy práce* na řádcích šablony práce.

## <a name="location-directives"></a>Směrnice skladového místa

Směrnice skladového místa jsou pravidla, která pomáhají identifikovat místa vyskladnění a umístění pro pohyb zásob. V transakce prodejní objednávky například směrnice skladového místa určuje, které zboží bude vydáno a kam bude umístěno. Směrnice skladového místa se skládají ze záhlaví a souvisejících řádků, a jejich vytvoření je možné na stránce **Směrnice skladového místa**.

Záhlaví každé směrnice skladového místa musí být přidruženo k *typu pořadí pracovních činností*, který určuje typ skladové transakce, pro kterou bude použita směrnice, jako například prodejní objednávky, doplnění nebo výdej surovin. *Typ práce* určuje, zda se směrnice skladového místa použije pro výdej nebo vložení práce, nebo pro některé další skladové procesy, jako například inventuru nebo změny stavu zásob. Je třeba zadat *pracoviště* a *sklad*. *Kód předpisu*, který určíte v záhlaví, slouží k propojení směrnice skladového místa k jedné nebo více šablonám práce. 

Pro šablony práce lze nastavit dotaz, který určuje, kdy je použita konkrétní směrnice skladového místa. Můžete například určit, že pokud má elektronická objednávka původ v prodejní objednávce, zásoby musí být vyskladněny z vyhrazené místo ve skladu. Systém používá pole **Pořadové číslo** k určení pořadí, ve kterém jsou posuzovány směrnice pro dostupné místo.

Řádky směrnice umístění stanoví další omezení aplikace pravidel hledání místa. Můžete zadat minimální a maximální množství, na které má být směrnice použita, a můžete určit, zda bude směrnice použita pouze pro specifickou skladovou jednotku. Například pokud je měrná jednotka palety, zboží v paletách může být vložit na určité skladové místo. Můžete také určit, zda lze množství rozdělit na více umístění. Stejně jako záhlaví směrnic skladového místa má každý řádek směrnice místa pořadové číslo určující pořadí, ve kterém jsou řádky posuzovány.

Směrnice skladového místa mají další úroveň podrobností: *akce směrnice skladového místa*. Můžete určit více akcí směrnice skladového místa pro každý řádek. Pořadové číslo se znovu použije k určení pořadí, ve kterém jsou akce posuzovány. Na této úrovni můžete nastavit dotaz a definovat tak způsob vyhledání nejlepšího skladového místa ve skladu. Také můžete použít předdefinované nastavení **Strategie** a najít tak optimální skladové místo.

Další informace o tom, jak vytvářet a konfigurovat směrnice o umístění, naleznete na stránce [Vytvořte směrnici o umístění](create-location-directive.md).

### <a name="how-location-directives-work"></a>Jak fungují směrnice skladového místa

Směrnice skladového místa určují, *kde* mají být položky vyzvednuty a *kam* mají být vloženy. Systém vyhodnotí směrnice skladového místa proti každému řádku práce a poté vybere umístění na základě podrobností řádku práce. Systém nejprve najde všechny směrnice skladového místa, které odpovídají konkrétnímu řádku práce (například jsou pro správný sklad a odpovídají dotazu). Poté postupně vyhodnotí směrnice, které našel.

> [!NOTE]
> Existují zvláštní případy, kdy je předem vybráno umístění pro výběr nebo vložení. Například během _registrace nákupu_ je první výběr vždy z místa, kde probíhá registrace. Dalším příkladem je *pohyb zásob podle šablony*, kde pracovník skladu vybere místo vyzvednutí a prostřednictvím směrnic skladového místa se naleznou pouze umístění pro vložení.

## <a name="additional-resources"></a>Další prostředky

- Video: [Podrobné prozkoumání konfigurace správy skladu](https://community.dynamics.com/365/b/techtalks/posts/warehouse-management-configuration-deep-dive-october-14-2020)
- Téma nápovědy: [Práce se směrnicemi skladového místa](create-location-directive.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]