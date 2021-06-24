---
title: Spravovat plánované objednávky
description: Toto téma obsahuje informace o postupu správy plánovaných objednávek. Popisuje, jak můžete aktualizovat stav plánovaných objednávek, upevnit je a zobrazit filtr plánovaných objednávek, které mají stejný stav, jako vybraná plánovaná objednávka.
author: roxanadiaconu
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqTransPo, ReqTransFirmLog
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7f16a666cef5625fb159265ddc7237ad0eb45927
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187643"
---
# <a name="maintain-planned-orders"></a>Spravovat plánované objednávky

[!include [banner](../includes/banner.md)]

Toto téma obsahuje informace o postupu správy plánovaných objednávek. Popisuje, jak můžete aktualizovat stav plánovaných objednávek, upevnit je a zobrazit filtr plánovaných objednávek, které mají stejný stav, jako vybraná plánovaná objednávka.

Naplánované objednávky lze spravovat v pracovním prostoru **Hlavní plánování**, na seznamu **Plánovaná objednávka** nebo na seznamech **Plánované výrobní zakázky**, **Plánované nákupní objednávky** a **Plánovaný převod**. 

## <a name="planned-order-status"></a>Stav plánované objednávky
Pole **Stav** lze použít ke sledování průběhu. Používají se následující hodnoty:

-   Když hlavní plánování vytvoří naplánované objednávky, mají stav **Nezpracovaná**.
-   Když se rozhodnete plánovanou objednávku nepotvrdit, můžete jí přiřadit stav **Dokončeno**.
-   Chcete-li potvrdit plánovanou objednávku, můžete její stav změnit na **Schváleno**. Plánované objednávky se stavem **Schváleno** jsou respektovány hlavním plánováním, takže nebudou během pozdějšího běhu hlavního plánování změněny ani odstraněny. Pro dosažení tohoto cíle logika plánování zkopíruje **schválené** plánované objednávky z původní verze plánu do nové verze plánu během hlavního plánování.

## <a name="firming-planned-orders"></a>Potvrzení plánovaných objednávek 
Při potvrzení plánovaných objednávek jsou vytvořeny reálné objednávky. Ty jsou známy také jako *vydané* nebo *otevřené* objednávky. Když je plánovaná objednávka potvrzena, přesune se do částí objednávek příslušného modulu.

Na stránce **plánované objednávky** můžete vybrat dvě možnosti potvrzení:

-   **Pevné** – tímto potvrdíte jednu nebo více vybraných plánovaných objednávek.
-   **Potvrdit vše** – Tato akce potvrdí všech plánovaných objednávek ve filtru. Když použijete možnost **Potvrdit vše**, nemusíte vybírat plánovanou objednávku, všechny plánované objednávky v rámci tohoto filtru budou potvrzeny. Tato možnost může být užitečná v případě, že potvrzujete vysoký počet plánovaných objednávek.

> [!NOTE]
> Můžete sledovat plánovanou objednávku, která byla potvrzena v **Historii potvrzení** v části **Formulář plánované objednávky > Zobrazení > Historie potvrzení**.

## <a name="parallelize-firming"></a>Paralelizovat potvrzení
Pokud plánujete potvrdit více objednávek najednou, může paralelní provedení zlepšit dobu provádění nebo výkon. Tato možnost je k dispozici při potvrzování více plánovaných objednávek pomocí možnosti **Potvrdit** nebo **Potvrdit vše**. K dispozici jsou následující parametry:

-   **Paralelizovat potvrzení** – Pokud je nastaveno **Ano**, proces potvrzování bude paralelizován s počtem podprocesů definovaných v poli **Počet podprocesů**.
-   **Počet podprocesů** – řídí počet podprocesů použitých k parallelize procesu potvrzování. Parametr se zobrazuje pouze tehdy, je-li volba **Paralelizovat potvrzení** nastavena na **Ano**.

> [!NOTE]
> Možnost pro **Paralelizovat potvrzení** je zobrazena pouze v případě, že jste vybrali více než jednu plánovanou objednávku pro potvrzení.

## <a name="additional-resources"></a>Další zdroje

[Přehled hlavních plánů](master-plans.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]