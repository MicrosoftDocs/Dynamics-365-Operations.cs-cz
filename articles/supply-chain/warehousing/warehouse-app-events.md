---
title: Události aplikace skladu
description: Toto téma popisuje zpracování událostí aplikace skladu používané ke zpracování zpráv o událostech aplikace skladu jako součást dávkové úlohy.
author: perlynne
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileDeviceQueueEvent
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d63cdea8917bed762bf8d970a408e5931aec48b7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837386"
---
# <a name="warehouse-app-event-processing"></a>Zpracování události aplikace skladu

[!include [banner](../includes/banner.md)]

Dávkové úlohy spuštěné v produktu Supply Chain Management mohou používat data z fronty pro zpracování událostí vydané v mobilní aplikaci Řízení skladu, aby podle potřeby reagovaly na signalizované události. Tato funkce přidává do fronty relevantní události v reakci na určité typy akcí prováděné pracovníky používajícími tuto aplikaci. Příkladem je, že při použití funkce *Vytvářet a zpracovat převodní příkazy z aplikace skladu* se záhlaví a řádky převodního příkazu vytvoří a aktualizují v back-endu, když v systému běží dávková úloha **Zpracovat události aplikace skladu**.

## <a name="enable-the-process-warehouse-app-events-feature"></a>Povolení funkce Zpracovat události aplikace skladu

Než budete moci použít tuto funkci, musíte ji povolit ve svém systému. Správci mohou pomocí stránky [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a povolit je v případě potřeby. Funkce Zpracovat události aplikace skladu je uvedena takto:

- **Modul** - Řízení skladu
- **Název funkce** – Zpracovat události aplikace skladu

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a>Nastavit dávkovou úlohu pro zpracování událostí aplikace skladu

### <a name="process-warehouse-app-events"></a>Zpracovat události aplikace skladu

Nastavte naplánovanou dávkovou úlohu pro zpracování událostí aplikace skladu pro vytvoření převodních příkazů a aktualizací řádků.

1. Přejděte na **Správa skladu \> Periodické úkoly \> Zpracovat události aplikace skladu**.
1. Otevře se dialogové okno Zpracovat události aplikace skladu. Rozbalte záložku s náhledem **Spustit na pozadí** a nastavte **Dávkové zpracování** na **Ano**.
1. Na pevné záložce **Spustit na pozadí** vyberte možnost **Opakování**.
1. Otevře se dialogové okno **Definujte opakování**. Nastavte plán běhu podle potřeby pro vaše podnikání.
1. Volbou **OK** se vraťte do dialogového okna **Zpracovat události aplikace skladu**.
1. Vyberte **OK** v dialogovém okně **Zpracovat události aplikace skladu** pro přidání dávkové úlohy do dávkové fronty.

## <a name="query-warehouse-app-events"></a>Dotazy na události aplikace skladu

Frontu událostí a zprávy o událostech generované mobilní aplikací Řízení skladu si můžete zobrazit přechodem na **Řízení skladu \> Dotazy a zprávy \> Protokoly mobilních zařízení \> Události aplikace skladu**.

## <a name="the-standard-event-queue-process"></a>Standardní proces fronty událostí

Fronta událostí skladové aplikace se obvykle používá s následujícím popsaným tokem:

1. Událost bude přidána do fronty se zprávou o události. Nová zpráva má zpočátku stav události **Čekání**, což znamená, že dávková úloha **Zpracovat události aplikace skladu** tuto zprávu nevyzvedne a nezpracuje.
1. Jakmile je stav zprávy aktualizován na **Ve frontě**, dávková úloha **Zpracovat události aplikace skladu** událost vyzvedne a zpracuje.
1. Dávková úloha aktualizuje stavy události buď na **Dokončeno**, nebo **Selhalo**, a to podle toho, zda byl požadovaný proces možný.
1. Když jsou všechny související zprávy o událostech **Dokončeno**, událost se odstraní z fronty.

 Podrobný příklad viz [Vytvoření převodního příkazu z procesu aplikace skladu](create-transfer-order-from-warehouse-app.md).

## <a name="handle-event-errors"></a>Zpracování chyb událostí

Je možné, že v rámci zpracování události skladu nebude aktivita požadované zprávy přijímat procesy z dávkové úlohy. V takovém případě se zpráva události změní na **Selhalo**. Můžete použít informace **Dávkový protokol**, abyste se dozvěděli proč a mohli podniknout kroky potřebné k nápravě případných problémů.

Podrobný příklad viz [Vytvoření převodního příkazu z aplikace skladu](create-transfer-order-from-warehouse-app.md).

Resetování zprávy „Selhalo“ o události aplikace:

1. Přejděte na **Řízení skladu \> Dotazy a zprávy \> Protokoly mobilních zařízení \> Události aplikace skladu**.
1. Na záložce s náhledem **Zprávy o událostech aplikace skladu** vyhledejte a vyberte relevantní událost, která se zobrazuje se stavem **Selhalo** ve sloupci **Stav události**.
1. Vyberte **Resetovat** z panelu nástrojů **Zprávy o událostech aplikace skladu**.
1. Pokračujte v práci, dokud se neresetují všechny relevantní zprávy.

Zprávu o události **Selhalo** můžete také odebrat pomocí možnosti **Odstranit** na panelu nástrojů **Zprávy o událostech aplikace skladu**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]