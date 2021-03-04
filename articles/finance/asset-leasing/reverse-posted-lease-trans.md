---
title: Stornování zaúčtované leasingové transakce
description: Toto téma vysvětluje, jak zrušit zaúčtovanou leasingovou transakci. Jakoukoli transakci vytvořenou prostřednictvím leasingu aktiv lze stornovat.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 259fd8f41eade1e873225f0d95c499c8cb8c1a6a
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4441357"
---
# <a name="reverse-posted-lease-transactions"></a>Stornování zaúčtované leasingové transakce

[!include [banner](../includes/banner.md)]

Jakoukoli transakci vytvořenou prostřednictvím leasingu aktiv lze stornovat. Transakce, které jsou stornovány prostřednictvím leasingu aktiv, aktualizují vaše data leasingu. Proto také aktualizují účetní hodnoty závazku z leasingu a používaný majetek.

Chcete-li vytvořit stornovací transakci pro leasing, postupujte takto.

1. Na stránce **Majetkové transakce** nebo **Odpovědnost za transakce** vyberte transakci a poté vyberte **Stornovat transakce**.
2. V dialogovém okně, které se zobrazí, můžete upravit datum, kdy bude zaúčtována stornovací položka. Ve výchozím nastavení je pole **Datum** je nastaveno na datum zaúčtování vybrané transakce. Stornující položku nelze zaúčtovat dříve než původní datum zaúčtování vybrané transakce.
3. Vyberte **OK**. Zaúčtuje se položka deníku, která stornuje záznam, který jste vybrali. Stornování je zobrazeno na stránce **Majetkové transakce** nebo **Transakce závazku** a čistý součet aktuálního zůstatku, který je na stránce zobrazen, se aktualizuje.

Když vyberete **Trasování storna**, zobrazí se dialogové okno, které zobrazuje původní transakce i stornované transakce spolu s propojeným číslem, které je známé jako *číslo trasování*. Aby bylo možné storna snáze pochopit a zlepšit viditelnost, můžete je sledovat také pomocí plánů leasingu.

Pole **Poslední číslo deníku** na stránce **Plán** zobrazuje čísla deníků transakcí. Když je transakce stornováno, toto pole je aktualizováno číslem deníku stornované transakce. Kromě toho je zaškrtnuto políčko **Stornováno** označující, že transakce byla zrušena, a je vybráno pole **Zaúčtováno**.

## <a name="revoke-a-reversed-transaction"></a>Odvolání stornované transakce

Chcete-li odvolat stornovanou transakci, postupujte takto.

1. Na stránce **Plán** nebo **Transakce** vyberte původní transakci.
2. Proveďte jeden z následujících kroků:

    - Pokud jste vybrali transakci na stránce **Plán**, postupujte podle pokynů pro vytvoření deníku v části [Vytvoření měsíčních záznamů deníku v dávce](create-monthly-journals-batch.md). Deník musíte zaúčtovat ručně.
    - Pokud jste vybrali transakci na stránce **Transakce**, vyberte **Stornovat transakci**. Zobrazí se zpráva s oznámením, že toto odvolání je odvoláním dřívějšího zrušení a že můžete upravit datum zaúčtování tohoto odvolání. Obecná obchodní ověření však ovlivňují data, která lze zadat v poli **Datum**. 

3. Vyberte **OK**. Zaúčtuje se položka deníku, která stornuje záznam, který jste vybrali. Stornování je zobrazeno na stránce **Transakce** a čistý celkový aktuální zůstatek se obnoví na hodnotu před prvním stornováním. Dopad, který mělo zrušení na zůstatky, je proto negován.

Když vyberete **Trasování storna**, zobrazí se dialogové okno, které zobrazuje původní transakce i stornované transakce spolu s propojeným číslem trasování.

Můžete také trasovat odvolání pomocí příslušné stránky **Plány**. Pole **Storno** je vymazáno, zatímco je vybráno pole **Deník zaúčtován**. Pole **Poslední číslo deníku** je dále aktualizováno číslem deníku transakce odvolání a pole **Číslo deníku** je aktualizováno číslem deníku storna.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]