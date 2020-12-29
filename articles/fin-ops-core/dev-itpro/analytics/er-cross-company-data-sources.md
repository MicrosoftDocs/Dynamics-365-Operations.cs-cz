---
title: Datové zdroje mezi více společnostmi v modulu Elektronické výkaznictví
description: Toto téma vysvětluje, jak je možné používat datové zdroje mezi více společnostmi v modulu Elektronické výkaznictví (ER).
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERModelMappingDesigner, ERFormatMappingLegalEntityFilterTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 1a5c05b65c9022220056947471e95b703d923dc5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680823"
---
# <a name="cross-company-data-sources-in-electronic-reporting-er"></a>Datové zdroje mezi více společnostmi v modulu Elektronické výkaznictví

[!include[banner](../includes/banner.md)]

Formáty v modulu Elektronické výkaznictví (ER) můžete navrhovat pro generování odchozích dokumentů v různých formátech. Při generování dokumentu formát ER volá zdroje dat, které byly nakonfigurovány v odpovídajícím mapování modelu ER. Aby bylo možné nakonfigurovat přístup k tabulkám aplikace pro načtení záznamu, můžete použít zdroje dat ER typu **záznamy tabulky**. Když je tabulka pro přístup sdílená (to znamená tabulka s uloženými daty bez identifikátoru společnosti), tento zdroj dat vrátí všechny záznamy. Když je tabulka přístupu závislá na společnosti (to znamená tabulka, kde jsou data uložená podle společností), vrátí tento zdroj dat pouze záznamy, které byly uloženy pro aktuální společnost (tj. kontext společnosti, ve kterém je spuštěný formát ER).

Každý zdroj dat typu **záznamy tabulky** v mapování modelu lze nyní označit jako zdroj dat mezi společnostmi. Proto můžete použít zdroje dat ER typu **záznamy tabulky** pro přístup k tabulkám aplikace pro načtení záznamu.

Pokud datový zdroj označíte jako mezi více společnostmi, dojde k následujícímu chování:

- Zdroj dat, který odkazuje na libovolnou sdílenou tabulku kromě CompanyInfo vrátí všechny záznamy, které existují odkazované tabulce. 
- Zdroj dat, který se vztahuje k tabulce CompanyInfo i přesto, že CompanyInfo je ve sdílené tabulce, nevrátí záznamy obsahující identifikátor společnosti v zadaném rozsahu.
- Zdroj dat pro jakoukoliv tabulku závislou na společnosti vrátí záznamy odkazované tabulky obsahující identifikátor společnosti v zadaném rozsahu.

V dialogovém okně dotazu systému, když je zapnutá možnost **požádat o dotaz** pro jakýkoli datový zdroj, který je označen jako mezi více společnostmi, je možné vybrat ručně jednu nebo více společností pro zahrnutí na kartu **Rozsah společnosti**.

> [!IMPORTANT]
> Podobně jako jiné filtry je filtr společnosti trvalý jako hodnota naposledy použitá pro dotazy při spuštění formátu ER. Jestliže změníte hodnotu mezi více společnostmi pro zdroj dat, filtr se nezmění automaticky. Pokud chcete použít jinou hodnotu mezi více společnostmi pro jiný zdroj dat, odstraňte odpovídající výběr konkrétního uživatele.

Pro každý zdroj dat, který je označen jako mezi více společnostmi, můžete vybrat záznamy, které použijete, pomocí funkcí **FILTER** a **WHERE** ve výrazu ER. Pole **dataAreaID** lze také použít jako identifikátor společnosti. V současné době je pole **dataAreaID** omezeno na následující typy podmínek při použití funkce **FILTER**:

- Jsou podporovány pouze podmínky, které mají jedno porovnání pole **dataAreaID**.
- Jsou povolena pouze porovnání, která mají výrazy nezávislé na záznamech položek v seznamu.

Následující výraz je tedy platný.

```ER Expression
FILTER (MyTable, MyTable.dataAreaID = $StringUserInputParameter)
While shown below expressions will not pass the validation:
FILTER (MyTable, MyTable.dataAreaID = MyTable2RecordsList.MyField)
FILTER (MyTable, 
    OR(
        MyTable.dataAreaID = $StringUserInputParameter1,
        MyTable.dataAreaID = $StringUserInputParameter2
    )
)
```

Výchozí rozsah obsahuje všechny společnosti aktuální aplikace. Může však být omezen. Pokud chcete omezit rozsah přístupu k datům mezi více společnostmi u jednoho formátu ER, přiřaďte formátu určitou organizační hierarchii. Když je hierarchie definovaná pro formát ER, jsou vráceny pouze záznamy pro právnické osoby, které jsou přítomny v přidělené hierarchii, přestože formát volá zdroje dat mezi společnostmi. Pokud definujete pro formát ER odkaz na hierarchii, který již existuje, je použit výchozí rozsah a formát volá zdroje dat mezi společnostmi. V takovém případě budou vráceny záznamy pro všechny společnosti v aplikaci.

Všimněte si, že když je zapnuta možnost **Použít koncept** pro přiřazení k jedné organizační hierarchii ER formátu, právnické osoby z pracovní verze této hierarchie budou použity k identifikaci rozsahu pro zdroje dat mezi společnostmi. Pokud pracovní verzi neexistuje, budou použity právnické osoby z poslední publikované verze této organizační hierarchie.

Všimněte si, že když je vypnutá možnost **Použít koncept** pro přiřazení k jedné organizační hierarchii ER formátu, právnické osoby z naposledy publikované verze organizační hierarchie budou použity k identifikaci rozsahu pro zdroje dat mezi společnostmi. Datum účinnosti organizačních hierarchií zatím v prostředí ER není podporováno.

Hierarchii lze přiřadit k formátu na konkrétní stránce, která je přístupné z pracovního prostoru ER nebo pomocí položky nabídky **Správa organizace \> Elektronické sestavy \> Filtr právnické osoby pro formáty**. Uživateli musí být uděleno oprávnění pro přístup na stránku **Udržovat filtry právnické osoby pro formát** (ERMaintainFormatMappingLegalEntityFilters). Omezení rozsahu právnických osob na základě hierarchie formátu se používá spolu s omezením, které může uživatel zadat ručně v dialogovém okně dotazu systému. Křížení těchto omezení je použito při spuštění formátu.

Další informace o této funkci zobrazíte přehráním Průvodce záznamem úloh **Záznamy pro přístup ER tabulek závislosti společnosti v režimu mezi více společnostmi**, který je součástí obchodního procesu komponenty službu a řešení 7.5.4.3 IT získání/vývoj (10677) obchodního procesu a mohou být staženy ze služby [Stažení softwaru Microsoft](https://go.microsoft.com/fwlink/?linkid=874684). Tento Průvodce záznamem úloh vás provede procesem konfigurace mapování modelu ER a formátu ER tak, aby byl možný přístup k tabulkám aplikace v režimu mezi více společnostmi.

Pro dokončení průvodce záznamem úloh stáhněte následující soubory.

- [Konfigurace modelu dat – ER CrossCompanyDataAccessModel.xml](https://go.microsoft.com/fwlink/?linkid=874111)
- [Konfigurace formátu ER – CrossCompanyDataAccessFormat.xml](https://go.microsoft.com/fwlink/?linkid=874111)
