---
title: Kusovníky a receptury
description: Tento článek obsahuje informace o kusovnících a vzorce, které jsou ústřední součástí definice produktů a variant produktu.
author: johanhoffmann
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMConsistOf, BOMDesigner, BOMTable, EcoResProductProcessManufacturingWorkspace, ProdBOM, ProdJournalTransBOM, ProdBOMCurrent, PmfBOMDesignerEditCoBy, ProdJournalPickingListLineSummary, ProdBOMOverview, PmfCoReqPlanning, EcoResProductProdTypeFormulaNoActiveFormulaFormPart, EcoResItemsMissingActiveRouteVersionFormPart, EcoResItemsProdTypeBOMExpiringBOMFormPart, BOMDesignerBOMVersion, BOMExpandPurch, BOMChangeLine, BOMExpandSales, EcoResItemsProdTypeBOMExpiringRouteFormPart, EngChgEcmBomDesigner, EngChgEcmProductBOMItemIdLookup, EngChgEcmProductBOMConsistOf, EngChgEcmBOMCopyDialog, EngChgEcmBomDesignerEditBom, BOMDesignerFilterDialog, BOMDesignerFilterDialog, BOMPartOf, BOMSetupReportFinish, EcoResItemsMissingActiveBOMVersionFormPart, BOMIdLookup, EcoResProductProdTypeFormulaNoActiveRouteFormPart, BOMExpandPurchRFQ, EngChgCaseRouteTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19331
ms.assetid: c19b437a-2de2-4728-9477-2bcb0c2b1f5e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 57a30aba3b0a37d939d0747b2dd305a92c82ae23
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887276"
---
# <a name="bills-of-materials-and-formulas"></a>Kusovníky a receptury

[!include [banner](../includes/banner.md)]

Tento článek obsahuje informace o kusovnících a vzorce, které jsou ústřední součástí definice produktů a variant produktu. Kusovníky a vzorce určují požadované materiály nebo látky pro konkrétní produkt. Vzorce také určují souběžné a vedlejších produkty, které jsou přijaty v rámci konkrétní výroby. 

## <a name="bills-of-materials"></a>Kusovník

Kusovník definuje součásti, které jsou potřebné pro výrobu produktu. Komponenty mohou být suroviny, polotovary a přísady. V některých případech může kusovník odkazovat na služby. Nejčastěji však kusovníky popisují *materiálové zdroje*, které jsou vyžadované.  

Kusovník, který se zkombinuje s postupem nebo výrobním tokem popisujícím operace a zdroje vyžadované k vytvoření produktu, tvoří základ výpočtu odhadovaných nákladů na produkt.  

Kusovník je samostatnou entitou, kterou definují následující informace:

-   ID BOM
-   Název kusovníku
-   Řádky kusovníku popisující součásti a látky
-   Verze kusovníku popisující produkt a období, pro které lze pro kusovník použít

Jeden kusovník popisuje jednu úroveň identifikovanou jedinečným ID. Komponenty mohou mít vlastní kusovníky, na které se odkazuje verzemi kusovníků. Celou hierarchii kusovníků konkrétního produktu můžete zobrazit a upravit v Návrháři kusovníku.

### <a name="formulas-co-products-and-by-products"></a>Receptury, souběžné produkty a vedlejší produkty

Receptura je podtyp kusovníku, který se obvykle používá pro procesní výrobu. Kromě komponent a látek popisuje receptura souběžné a vedlejší produkty. V samotné verzi vyžaduje definice souběžných a vedlejších produktů receptury verzi receptury. Receptura se obvykle definuje pro jeden konkrétní dokončený produkt (recepturu nebo položku plánování), který se definuje ve verzi receptury.

### <a name="boms-in-the-product-lifecycle"></a>Kusovníky v životním cyklu produktu

V životním cyklu produktu lze vytvořit mnoho typů kusovníků z různých důvodů:

-   **Náčrtový/konceptní kusovník** – tento kusovník poskytuje hrubý odhad požadovaných materiálů v počáteční fázi návrhu a usnadňuje hrubý odhad nákladů a odhadované atributy produktu. Tento kusovník obvykle nepoužívá podnikové zdroje plánování (ERP).
-   **Vývojový kusovník** – tento kusovník se obvykle používá při návrhu produktů, které jsou založeny na existujících portfoliích produktů. Vývojové kusovníky jsou strukturovány tak, aby zjednodušily proces návrhu a seskupily komplexní produkty do vývojových modulů. U jednoduchých produktů lze použít vývojové kusovníky při samotném výrobním procesu. U jiných produktů je však nutné převést vývojový kusovník na výrobní kusovník. Vývojové kusovníky se v hierarchii kusovníků zpravidla zobrazují jako fiktivní. Přestože lze vývojové kusovníky použít k plánování a provádění výrobních operací, tento přístup může vést k neefektivitě, zejména u opakujících se operace, při kterých se vytváří mnoho objednávek.
-   **Plánovací kusovník** – tento kusovník se používá k plánování požadavků na materiál. Poptávka po komponentech a látkách se vypočítává podle poptávky po hotových produktech. Podobně jako nákladové kusovníky mohou plánovací kusovníky představovat specifickou kombinaci materiálu, který se v období používá.
-   **Výrobní kusovník** – jedná se o kusovník, který se skutečně používá pro určitou výrobu. Výrobní kusovník musí brát v úvahu zdroje skutečně používané pro výrobu produktu. Při vytvoření výrobní zakázky, dávkové objednávky nebo kanbanu se jednotlivé úrovně kusovníku zobrazují jako fiktivní, jsou sbaleny do jedné úrovně a rozprostřeny po operacích pro objednávku.
-   **Nákladový kusovník** – tento kusovník se používá k výpočtu odhadovaných nákladů na produkt. Nákladový kusovník můžete například použít, když se používají standardní náklady nebo se vypočítávají odhadované plánované náklady určitého produktu. Nákladové kusovníky mohou odkazovat na konkrétní kombinací materiálů a zdrojů, která se má použít. Nákladové kusovníky tedy můžete použít k vytvoření zástupce odhadovaných nákladů za období a abyste se vyhnuli odchylkám v průběhu času.

Druhy kusovníku, které skutečně použijete pro implementaci, závisí na implementaci a také na obchodních scénářích a požadavcích. V jednoduché implementací lze plánovací kusovníku, výrobní kusovník a nákladový kusovník modelovat jako jeden kusovník. V prostředí s častými technologickými změnami a více alternativními postupy bude pravděpodobně nutné použít více typů kusovníků.

### <a name="approval-of-boms-and-formulas"></a>Schválení kusovníků a receptur

Každý kusovník a recepturu lze samostatně schválit nebo zamítnout. Schválení kusovníků nebo receptur obvykle probíhá po schválení první příslušné verze kusovníku. V některých obchodních scénářích však mohou být tato schválení jinými fázemi procesu a mohou zahrnovat jiné vlastníky procesů.  

Všimněte si, že v případě neschváleného kusovníku se všechny související verze kusovníku také zamítnou.

## <a name="bom-and-formula-versions"></a>Verze kusovníku a receptury
K úpravě na varianty produktu, které lze vyrobit konkrétní Kusovníku nebo receptury, je nutné vytvořit verze Kusovníku nebo verze receptury. Platnost verzí kusovníku a verzí receptury lze omezit podle období, množství, pracoviště, konkrétních dimenzí produktu a dalších kritérií. Verze receptur mají další důležité atributy, například výnosnost, definice souběžných a vedlejších produktů a pokyny k rozdělení nákladů pro recepturu.

### <a name="approval-of-bom-and-formula-versions"></a>Schválení verzí kusovníku a receptury

Verze kusovníku se musí před použitím v plánovacím nebo výrobním procesu schválit. Po schválení verze kusovníku lze také schválit související kusovník v závislosti na výběru uživatele a oprávněních ověřování. Všimněte si, že verzi kusovníku lze schválit pouze v případě, že se schválí související kusovník.

### <a name="activation-of-the-default-bom-or-formula-version"></a>Aktivace verze výchozího kusovníku nebo receptury

Chcete-li nastavit konkrétní kusovník nebo recepturu jako výchozí verzi kusovníku nebo receptury, která se použije při hlavním plánování nebo k vytvoření výrobních zakázek, je nutné aktivovat verzi. Když je verze aktivována, ověří se její jedinečnost pro daná omezení (například období, pracoviště nebo množství). Je-li verze, kterou se pokoušíte aktivovat, v konfliktu s již aktivní verzí, zobrazí se chybová zpráva. Musíte pak buď deaktivovat verzi konfliktní verzi, nebo upravit omezení verze (obvykle období), abyste zabránili nejednoznačné aktivaci.

### <a name="product-change-with-case-management"></a>Změna produktu se správou případu

Případ změny produktu k schválení a aktivaci nových nebo změněných kusovníků a verzí kusovníků představuje snadný způsob, jak zobrazit přehled omezení verze kusovníku. Můžete rovněž schválit a aktivovat všechny kusovníky a receptury, které souvisejí s určitou změnou pro jediné datum aktivace.

### <a name="alternative-bom-versions"></a>Alternativní verze kusovníku

V určitých případech by se aktivní verze kusovníku nebo verze receptury neměly používat v prognózách, prodeji nebo nadřazeném produktu. V tomto případě můžete vybrat konkrétní schválený kusovník jako součást požadavku (řádek prognózy, řádek prodeje nebo řádek kusovníku), pokud schválená verze kusovníku nebo verze receptury existuje pro alternativní kusovníku nebo recepturu.  

Po vytvoření plánovaných objednávek, výrobních zakázek nebo kanbanů může plánovač nebo vedoucí dílny použít schválenou verzi kusovníku, která je platná pro požadované plánované výrobní datum, k plánování nebo výrobě určitého produktu. Použitá verze kusovníku nemusí být aktivovaná jako výchozí verze kusovníku.

## <a name="bom-and-formula-lines"></a>Řádky kusovníku a receptury
Řádek kusovníku se vytváří pro každý materiál, službu a látku. Řádek definuje plánovanou spotřebu zadané varianty produktu a také různé atributy, které souvisí s plánovanou spotřebou.  

Řádky kusovníku mohou mít následujících typů řádků: **Položka**, **Fiktivní**, **Doložená dodávka**, **Dodavatel**.

### <a name="item"></a>Položka

Typ řádku **Položka** vyberte pro materiály a služby, které se přímo spotřebovávají a nevyžadují další rozpad nebo doloženou dodávku.

### <a name="phantom"></a>Fiktivní

Typ řádku **Fiktivní** vyberte, pokud chcete rozpadnout libovolné položky kusovníku na nižší úrovni, které jsou obsaženy v řádku kusovníku. V Hlavním plánování při výpočtu plánovaných nákladů nebo při odhadu výrobní zakázky, která používá řádky kusovníku typu **Fiktivní**, odkazuje řádek v nadřazeném kusovníku k variantě produktu, ve které je fiktivní kusovník nahrazený položkami komponentů uvedenými na řádcích kusovníku v daném kusovníku, jak je určeno na základě odpovídající aktivní verze kusovníku této varianty produktu. Má-li varianta produktu použitelný aktivní postup, operace tohoto postupu se sloučí do nadřazeného postupu.  

Všimněte si, že fiktivní se obvykle používají pro zjednodušení výrobního procesu. Plošné používání fiktivních kusovníků na velkém počtu úrovní má vliv na výkon, zejména v případě výrobních scénářů, které se velmi často opakují. Chcete-li zlepšit výkon, vyhněte se složité hierarchii fiktivních kusovníků. Místo toho použijte předem rozložené výrobní kusovníky a postupy.

### <a name="pegged-supply"></a>Doložená dodávka

Vyberte typ řádku **Doložená dodávka**, pokud chcete vytvořit odvozenou výrobu, kanban události řádku kusovníku nebo přímou nákupní objednávku pro všechny varianty produktu, které odkazuje řádek kusovníku. Odvozená výroba, kanban události nebo nákupní objednávka se vytvoří, když provedete odhad nákupní objednávky. Pro spotřební výrobní zakázku se automaticky rezervují povinná množství položek.

### <a name="vendor"></a>Dodavatel

Vyberte řádek **Dodavatel**, pokud výrobní proces používá subdodavatele a pokud chcete pro tohoto subdodavatele automaticky vytvořit dílčí výrobu nebo prodejní objednávku.  

**Poznámka týkající se subdodavatelských operací v kusovníku:** servis nebo práce prováděná tímto subdodavatelem se musí vytvořit jako servisní položka, která se sleduje ve skladu. Servisní položku je nutné připojit k nadřazené položce jako řádek kusovníku. Postup musí obsahovat operaci, která je přiřazena k provoznímu prostředku subdodavatele.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]