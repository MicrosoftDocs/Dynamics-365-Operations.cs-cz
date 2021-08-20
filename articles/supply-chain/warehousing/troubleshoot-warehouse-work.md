---
title: Odstraňování problémů s prací skladu
description: Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při práci s prací skladu v Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: f9dbc1e043de5c8f840b291b652ec522c9f1eb6a622e8dab88ced3fa91570e8e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6775452"
---
# <a name="troubleshoot-warehouse-work"></a>Odstraňování problémů s prací skladu

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při práci s prací skladu v Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-cant-move-license-plates-that-have-serial-number-items-when-blank-issue-and-blank-receipt-are-allowed-on-the-tracking-dimension-group"></a>Nemohu přesouvat registrační značky, které mají položky sériového čísla, když je ve skupině dimenze sledování povolen prázdný výdej a prázdná příjemka.

### <a name="issue-description"></a>Popis problému

Registrační značku nelze přesunout pomocí položky nabídky **Přesun**, pokud má sériové číslo nastavení *Prázdný výdej povolen* a *Prázdná příjemka povolena* ve skupině dimenze sledování a pokud je na stejném místě více registračních značek, některé mají sériová čísla a některé je nemají.

### <a name="issue-resolution"></a>Řešení problému

Tento problém bude vyřešen změnami, které jsou nasazeny v [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687). Tyto změny způsobí, že je pole **Sériové číslo** nepovinné, pokud jsou povoleny prázdné příjemky a prázdné výdeje.

## <a name="i-receive-the-following-error-message-in-the-warehouse-management-mobile-app-when-i-process-movements-the-inventory-owner-1-is-not-allowed-in-this-process"></a>Při zpracování pohybů se mi v mobilní aplikaci Řízení skladu zobrazí následující chybová zpráva: „Vlastník inventáře %1 v tomto procesu není povolen.“

### <a name="issue-description"></a>Popis problému

Sledovací dimenze **Vlastník** chybí, když se mobilní aplikaci Řízení skladu používá k provádění přesunů. Pravidelný deník přesunů zásob od klienta Supply Chain Management nejspíš funguje podle plánu a lze ho zaúčtovat, pouze pokud je vyplněna dimenze **Vlastník**.

### <a name="issue-resolution"></a>Řešení problému

Společnost Microsoft vyhodnotila tento problém a zjistila, že jde o omezení funkcí. V současné době procesy správy skladu podporují pouze zásoby, které jsou ve vlastnictví právnické osoby.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]