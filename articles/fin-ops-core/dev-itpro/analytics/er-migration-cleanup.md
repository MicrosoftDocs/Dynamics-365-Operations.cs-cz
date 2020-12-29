---
title: Vyčištění migrace elektronického výkaznictví
description: Toto téma vysvětluje, jak můžete pomocí funkce čištění migrace ER vyřešit problémy se šablonami ER.
author: NickSelin
manager: AnnBe
ms.date: 04/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, ERParameters, ERMigrationCleanup
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: edb60f247b2bd6cc4ecd514e3e85bafbb681788d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686361"
---
# <a name="er-migration-cleanup"></a>Vyčištění migrace elektronického výkaznictví 

[!include[banner](../includes/banner.md)]

Při správě instancí modulu Finance se můžete rozhodnout migrovat aktuální instanci do jiného umístění. Můžete například migrovat instanci výroby do nového prostředí sandbox. Pokud jste nakonfigurovali platformu elektronického výkaznictví (ER) pro ukládání šablon v úložišti objektů Blob Microsoft Azure, bude tabulka **DocuValue** v novém prostředí sandbox odkazovat na instanci ukládání objektů Blob v produkčním prostředí. K této instanci však nelze přistupovat z prostředí izolovaného prostoru (sandbox), protože proces migrace nepodporuje migraci artefaktů v úložišti objektů BLOB. Spíše se očekává, že v novém sandboxovém prostředí odkazujete na instanci úložiště objektů Blob v sandboxovém prostředí, které dosud nezískalo šablony ER.

Pokud se pokusíte spustit formát ER, který používá šablonu pro generování obchodních dokumentů, dojde k výjimce a zobrazí se upozornění na chybějící šablonu. Také budete navedeni pomocí nástroje čištění migrace ER k tomu, abyste odstranili a následně znovu importovali konfiguraci formátu ER obsahující šablonu.

[![Spuštění formátu ER](./media/er-migration-cleanup-run.png)](./media/er-migration-cleanup-run.png)

Obdobnou chybu dostanete, pokud přejdete na stránku **Konfigurace** (**Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**) a ve stromu konfigurací se pokuste odstranit konfiguraci formátu ER, která používá šablonu.

[![Odstranění formátu ER](./media/er-migration-cleanup-delete.png)](./media/er-migration-cleanup-delete.png)

Chcete-li vyřešit problémy se šablonami ER, ke kterým nemáte přístup, proveďte následující kroky.

1.  Přejděte na stránku **Správa organizace** \> **Pravidelné** \> **Čištění migrace**.
2.  Vyberte konfiguraci formátu ER, kterou nelze provést nebo odstranit.
3.  Zvolte **Odstranit**.
4.  Potvrďte odstranění vybrané konfigurace formátu ER.
5.  [Importujte](download-electronic-reporting-configuration-lcs.md) odstraněnou konfiguraci formátu ER pro aktuální finanční instanci.

## <a name="applicability"></a>Použitelnost

> [Důležité] Možnost **Vyčištění migrace** je zaměřena pouze na konfigurace formátu ER, které obsahují nepřístupné šablony ER. Když odstraníte konfiguraci formátu ER pomocí možnosti **Vyčištění migrace**, ER odstraní šablony, které souvisí s konfiguračními artefakty v jediné databázi aplikací. Existence příslušných fyzických souborů v úložišti objektů Blob není ověřena. Místo toho se předpokládá, že žádné neexistují. Nepoužívejte proto možnost **Vyčištění migrace** jako alternativu k možnosti vymazání konfigurace ER na stránce **Konfigurace**. Možnost **Vyčištění migrace** proto používejte pouze tehdy, když možnost odstranění konfigurace ER na stránce **Konfigurace** selhala.
>
> Když odstraníte konfiguraci formátu ER pomocí možnosti **Vyčištění migrace** v době, kdy je odkazovaná šablona dostupná v úložišti objektů Blob, odstraníte pouze související konfigurační artefakty v databázi aplikací. Fyzický soubor šablony v úložišti objektů Blob zůstává. Přepisování souborů v úložišti objektů Blob již není povoleno. Další informace naleznete v článku [KB4557217](https://fix.lcs.dynamics.com/Issue/Details?kb=4557217). Kromě toho již nebudete moci znovu importovat konfigurace odstraněné pomocí vyčištění migrace v tomto prostředí. Chcete-li tento problém vyřešit, musíte najít odpovídající soubor v úložišti objektů Blob a ručně jej odstranit.

[![Import formátu ER](./media/er-migration-cleanup-import.png)](./media/er-migration-cleanup-import.png)

Podobný problém může nastat, pokud migrujete instanci aplikace do jiného umístění, které bylo více než jednou použito jako cíl migrace a pro které úložiště objektů Blob již obsahuje soubory šablony ER.

Vzhledem k tomu, že je možné provést několik konfigurací formátu ER, může být tento proces časově náročný. Proto je upřednostňováno použití funkce [Záložní úložiště šablon ER](er-backup-storage-templates.md) k automatickému obnovení šablon s poškozenými referencemi.
