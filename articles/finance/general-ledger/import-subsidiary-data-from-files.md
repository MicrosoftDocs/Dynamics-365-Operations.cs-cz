---
title: Import dat dceřiné společnosti ze souborů
description: Toto téma vysvětluje, jak připravit data z externích systémů tak, aby je bylo možné importovat do Microsoft Dynamics 365 Finance.
author: jinniew
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 4be1e748724331c4e2089da8a08a9ac7e5cf88a2ac6d3d89b37b9fcd4480f516
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6727293"
---
# <a name="import-subsidiary-data-from-files"></a>Import dat dceřiné společnosti ze souborů

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak připravit data z externích systémů tak, aby je bylo možné importovat do Microsoft Dynamics 365 Finance. Používáte stránku **Konsolidace s importem** (**Konsolidace \> Konsolidace s importem**) pro přípravu přenosu doplňkových dat z externích systémů.

1. Vytvoření dceřiné právnické osoby pro konsolidaci. Další informace, jak vytvořit právnické osoby, najdete v části [Vytvoření právnícké osoby](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md). Další informace viz [Připrava právnické osoby pro použití v procesu konsolidace](prepare-company-for-consolidation.md) a [Založení dceřiné právnické osoby ke konsolidaci](set-up-subsidiary-company-for-consolidation.md).

2. Připravte soubor, který bude obsahovat importovaná data. Další informace procesu importu naleznete v tématu [Přehled úloh importu a exportu dat](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).
3. Exportujte data do souboru podle pokynů v postupu „Proces importu / exportu dat“ v [Přehledu úloh importu a exportu dat](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md). Tento postup můžete použít ke konsolidaci dat z jiné instance Dynamics 365 Finance nebo z Dynamics 365 Business Central. Pokud importujete data z externích systémů, musí být data ve formátu popsaném v [Exportu dat dceřiné společnosti do souborů](export-subsidiary-data-to-file.md).
4. Přejděte na **Konsolidace \> Online konsolidace**. Na stránce **Konsolidace s importem** na kartě **Kritéria** zadejte podrobnosti sestavy nebo importu nastavením následujících polí.

    | Pole                                 | Hodnota pro sestavu | Hodnota pro import |
    |---------------------------------------|----------------------|----------------------|
    | popis                           | Nelze použít | Zadejte popis identifikující import. |
    | Hlavní účet                          | Definujte rozsah účtů, které by měl přehled obsahovat. Pokud nedefinujete rozsah, budou zahrnuty všechny účty. | Definujte rozsah účtů, které by měl import obsahovat. Pokud nedefinujete rozsah, budou zahrnuty všechny účty. |
    | Období konsolidace                  | Definujte rozsah dat, která chcete konsolidovat. | Definujte rozsah dat, která chcete konsolidovat. |
    | Zahrnout skutečné částky                | Tuto možnost nastavte na **Ano**, chcete-li zahrnout skutečné hodnoty. | Tuto možnost nastavte na **Ano**, chcete-li zahrnout skutečné hodnoty. |
    | Zahrnout rozpočtové částky                | Tuto možnost nastavte na **Ano**, chcete-li zahrnout částky rozpočtu do konsolidací. | Tuto možnost nastavte na **Ano**, chcete-li zahrnout částky rozpočtu do konsolidací. |
    | Znovu sestavte zůstatky během konsolidace | Tuto možnost nastavte na **Ano**, pokud by proces opětovného sestavení měl zcela vyčistit zůstatek a nové záznamy a znovu vytvořit zůstatek od počátku. | Tuto možnost nastavte na **Ano**, pokud by proces opětovného sestavení měl zcela vyčistit zůstatek a nové záznamy a znovu vytvořit zůstatek od počátku. |
    | Rozpočtové modely                         | Nelze použít | Pokud jste se rozhodli importovat částky rozpočtu, zadejte rozpočtové modely, které chcete konsolidovat. |
    | Typ rozpočtové sazby                      | Nelze použít | Zadejte typ směnného kurzu rozpočtu. |

6. Pokud máte různé účetní měny, použijte pole na kartě **Převod měn** pro konfiguraci převodu, který se provádí během konsolidace.

    | Pole                      | popis |
    |----------------------------|-------------|
    | Zdrojová právnická osoba        | Vyberte právnickou osobu, ze které importujete. |
    | Zúčtovací měna zdroje | Tato výchozí měna je měna přidružená ke zdrojové právnické osobě, kterou jste vybrali v poli **Zdrojová právnická osoba**. |
    | Účty od do       | Definujte rozsah účtů, které se mají importovat ze zdrojové právnické osoby. |
    | Typ směnného kurzu         | Vyberte typ směnného kurzu. Typy směnných kurzů jsou přiřazeny při vytváření hlavního účtu. Další informace naleznete v tématu [Vytvoření hlavního účtu](tasks/create-main-account.md). |
    | Použít směnný kurz z   | Zadejte datum pro použití směnného kurzu platného k tomuto datu. Případně zadejte hodnotu, která by měla být použita jako směnný kurz. |
    | Směnný kurz              | Výchozí hodnota závisí na typu směnného kurzu, který jste vybrali v poli **Typ směnného kurzu**. Pokud jste zadali uživatelem definovaný směnný kurz, můžete definovat kurz. |

7. Nastavte možnost **Spustit na pozadí** na **Ano**, chcete-li umožnit spuštění procesu importu na pozadí.
8. Nastavte možnost **Dávkové zpracování** na **Ano**, chcete-li spustit konsolidaci jako dávkovou úlohu v konkrétní čas. Chcete-li konsolidaci spustit okamžitě, vyberte **OK**. 

Transakce a zůstatky, které byly v dceřiných společnostech označeny ke konsolidaci, budou přidány na příslušné účty konsolidované právnické osoby.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]