---
title: "Import a udržování transakce platební karty"
description: "Toto téma vysvětluje postup, jak importovat a udržovat transakce platební karty týkající se výdajů. Tyto transakce lze nastavit tak, aby byly automaticky importovány v opakovaném plánování, nebo ručně importovány podle potřeby."
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e640c9e44add5599be4a2e381b4ffd81f212889c
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="import-and-maintain-credit-card-transactions"></a>Import a udržování transakce platební karty

[!include [banner](../includes/banner.md)]

Transakce platební karty související s výdaji lze nastavit tak, aby byly automaticky importovány v opakujícím se plánu. Popřípadě lze transakce ručně importovat podle potřeby. Transakce platebních karet jsou importovány prostřednictvím datové entity Transakce platebních karet.

Další informace o datových entitách naleznete v tématu [Datové entity](../../dev-itpro/data-entities/data-entities.md).

## <a name="import-credit-card-transactions"></a>Importovat transakce platebních karet

1. Na stránce **Transakce platebních karet** vyberte **Importovat transakce**. Pokud otevíráte správu dat poprvé, systém musí aktualizovat seznam datových entit předtím, než můžete pokračovat.
2. V poli **Název** zadejte jedinečný popis úlohy importu.
3. V poli **Formát dat zdroje** vyberte formát souboru, který obsahuje transakce platebních karet k importu.
4. Vyberte **Odeslat**a poté vyhledejte a vyberte soubor, který chcete importovat.
5. Po odeslání souboru ověřte mapování souboru transakcí platebních karet a sloupce datové entity Transakce platebních karet pomocí výběru odkazu **Zobrazit mapu** na dlaždici. Pokud došlo k chybám mapování nebo pokud musíte změnit mapování, proveďte změny mapování buď z karty **Vizualizace mapování** nebo z karty **Podrobnosti mapování**.
6. Chcete-li automatizovat transakce platebních karet, vyberte možnost **Vytvořit opakovanou datovou úlohu**. Pak lze nastavit opakování, které definuje, jak často mají být importovány transakce platebních karet. Po dokončení zvolte **OK**.
7. Chcete-li nyní importovat vybraný soubor, zvolte **Importovat**.
8. Při výskytu chyb během importu můžete zobrazit protokol provádění nebo fázování dat chyby, abyste zjistili chyby, které je nutné opravit k zajištění úspěšného importu.

> [!NOTE]
> Pokud je nutné importovat více než jeden formát souborů, je nutné vytvořit úlohy importu pro každý typ formátu.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Opětovně přiřazení transakcí platebních karet pro zrušené zaměstnance

Po ukončení záznamu zaměstnance je zakázán zaměstnancův účet služby Active Directory Domain Services (AD DS). Mohou však existovat aktivní transakce platební karty, které musí být ještě zaneseny do výdajů a uhrazeny. Ze stránky **Transakce platebních karet** můžete opět přiřadit zaměstnance k libovolné transakci platební karty, pokud byl související zaměstnanec propuštěn.

Vyberte jednu nebo více transakcí platebních karet a poté vyberte **Opětovně přiřadit transakce**. Poté můžete vybrat jiného zaměstnance, ke kterému přiřadíte transakce platebních karet. Poté, co opět přiřadíte transakce platební karty, můžete je vybrat pro sestavu výdajů a zaplatit běžným procesem pro uhrazení vyúčtování výdajů.

