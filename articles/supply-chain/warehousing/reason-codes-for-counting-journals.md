---
title: Kódy důvodů pro inventury zásob
description: Toto téma popisuje, jak nastavit a použít kódy důvodů pro úlohy účtování.
author: Mirzaab
manager: tfehr
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCountingReasonCodePolicy, InventCountingReasonCode
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 1025dd00db2e8b87e3c76e3047a7cf470a2d6641
ms.sourcegitcommit: 8cbaeb6443ce47a4c4bc02b5e1a1212eb0056b38
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/22/2020
ms.locfileid: "3829794"
---
# <a name="reason-codes-for-inventory-counting"></a>Kódy důvodů pro inventury zásob

[!include [banner](../includes/banner.md)]

Kódy důvodů umožňují analyzovat výsledky procesu inventury a jakýkoli nesoulad, který se vyskytne během tohoto procesu. Můžete určit důvod pro provádění inventury, například rozbitou paletu nebo úpravu zásob, založenou na vzorku zásob.

## <a name="recommendation"></a>Doporučení

Před nastavením systému doporučujeme nejprve definovat strategii pro práci s kódy důvodu. Zkuste například zodpovědět následující otázky:

- Měly by být kódy důvodů povinné na skladech?
- Měly by být kódy důvodů povinné nebo volitelné na některých položkách?
- Kolik kódů důvodů vyžadujete?
- Jak by měli uživatelé čteček čárových kódů používat kódy důvodů? Měly by být kódy důvodů předvybrané, povinné nebo bez možnosti úpravy?
- Vyžadují pracovníci skladu různé chování kódů důvodů na mobilních čtečkách? Je-li odpověď ano, můžete vytvořit další položky nabídky a přiřadit je k různým osobám.

## <a name="where-reason-codes-apply"></a>Kde se kódy důvodů používají

Můžete vytvořit více zásad kódů důvodů a každá zásady kódů důvodů může mít dvě zásady kódů důvodu inventury. Zásady kódů důvodů inventury lze použít na úrovni skladu nebo na úrovni položky.

## <a name="set-up-reason-code-policies"></a>Nastavení zásad kódů důvodů

1. Vyberte **Řízení zásob** \> **Nastavení** \> **Zásoby** \> **Zásady kódů důvodů inventury** a vytvořte novou zásadu kódů důvodů.
2. V poli **Typ kódu důvodů inventury** vyberte buď **Povinné** nebo **volitelné** a určete, zda výběr kódu důvodů má být volitelná nebo povinná akce v jednom z následujících deníků inventur:

    - Cyklická inventura (mobilní zařízení)
    - Místní inventura (mobilní zařízení)
    - Prahová inventura (mobilní zařízení)
    - Příchozí úprava (mobilní zařízení)
    - Odchozí úprava (mobilní zařízení)
    - Deník inventur (plně funkční klient)

Můžete také nastavit kódy důvodů pro jednotlivé sklady a produkty. Nastavení kódů důvodů pro produkty může nebrat v úvahu nastavení skladů.

## <a name="mandatory-reason-codes"></a>Povinné kódy důvodů

Pokud je nastaven parametr **Povinné** v konfiguraci kódů důvodů pro sklady pro nebo položky, deník inventur nelze dokončit a uzavřít, dokud neí zadán kód důvodu.

### <a name="set-up-reason-codes-for-warehouses"></a>Nastavení kódů důvodů pro sklady

1. Zvolte postupně možnosti **Řízení zásob** \> **Nastavení** \> **Rozdělení zásob** \> **Sklady**.
2. Na kartě **Sklad** v poli **Zásady kódu důvodů inventry** vyberte některou z následujících možností:

    - **Prázdné** – Parametr, který je nastaven pro položku, se používá k určení, zda deníky inventur jsou pro produkt povinné.
    - **Povinné** – Kód důvodu je vyžadován vždy na denících inventury pro sklad.
    - **Volitelné** – Kód důvodu není vyžadován na denících inventury pro sklad.

### <a name="set-up-reason-codes-for-products"></a>Nastavení kódů důvodů pro produkty

1. Zvolte **Řízení informací o produktech** \> **Produkty** \> **Uvolněné produkty**.
2. Na kartě **Produkt** vyberte **Zásady kódu důvodů inventry** a poté vyberte některou z následujících možností:

    - **Prázdné** – Parametr, který je nastaven pro sklad, se používá k určení, zda deníky inventur jsou pro produkt povinné.
    - **Povinné** – Kód důvodu je vyžadován vždy na denících inventury pro produkt. Toto nastavení přepíše všechna nastavení kódu důvodu na úrovni skladu.
    - **Volitelné** – Kód důvodu není vyžadován na denících inventury pro produkt. Toto nastavení přepíše všechna nastavení kódu důvodu na úrovni skladu.

### <a name="use-reason-codes-in-counting-journals"></a>Použití kódů důvodů v deníku inventury

V deníku inventur můžete přidat kódy důvodů pro inventury následujících typů:

- Cyklická inventura
- Místní inventura
- Prahová inventura
- Příchozí úprava
- Odchozí úprava

Kódy důvodů jsou přidány do řádků deníku v denících inventur tyou **Deník inventur**.

1. Zvolte **Řízení zásob** \> **Položky deníku** \> **Inventura zboží** \> **Inventura**.
2. V podrobnostech řádku deníku inventury v poli **Kód důvodů inventury** vyberte možnost.

### <a name="view-the-counting-history-as-its-recorded-by-reason-codes"></a>Zobrazení historie inventur, jak ji zanamenaly kódy důvodů

- Vyberte **Řízení zásob** \> **Dotazy a sestavy** \> **Historie inventury** a pak v poli **Kód důvodů inventury** zobrazte historii inventury, která byla zaznamenána pomocí kódu důvodu.

### <a name="use-a-reason-code-for-a-quantity-adjustment"></a>Použití kódu důvodů pro úpravu množství

1. Na stránce **Zásoby na skladě** vyberte **Upravit množství**. Můžete otevřít stránku **Zásoby na skladě** několika způsoby. Například zvolte **Řízení zásob** \> **Dotazy a sestavy** \> **Zásoby na skladě**.
2. Zvolte **Upravit množství**a pak v poli **Kód důvodů inventury** vyberte kód důvodu.

### <a name="configure-reason-codes-for-mobile-device-menu-items"></a>Konfigurace kódů důvodů pro položky nabídky mobilního zařízení

Můžete konfigurovat kódy důvodů pro jakýkoliv typ inventury na položce nabídky mobilního zařízení. Konfigurace položky nabídky mobilního zařízení obsahuje následující informace:

- Zda je kód důvodu zobrazen pro pracovníka na mobilním zařízení při inventuře.
- Výchozí kód důvodu, který se zobrazí na položce nabídky mobilního zařízení.
- Zda uživatel může upravit kód důvodu.

### <a name="set-up-reason-codes-on-a-mobile-device"></a>Nastavení kódů důvodů na mobilním zařízení

1. Přejděte do nabídky **Řízení skladu** \> **Nastavení** \> **Mobilní zařízení** \> **Položky nabídky mobilního zařízení**.
2. Na kartě **Cyklická inventura** zvolte **Cyklická inventura**.
3. V poli **Výchozí kód důvodů inventury** nastavte výchozí kód důvodu, který má být zaznamenán po provedení inventury pomocí položky nabídky mobilního zařízení.
4. V poli **Zobrazit kód důvodů inventury** vyberte **Řádek** pro zobrazení kódu důvodu poté, co je zaznamenána každá odchylka. Popřípadě zvolte **Skrýt**, pokud nemá být kód důvodu zobrazen.
5. Nastavte možnost **Upravit kód důvodů inventury** buď na možnost **Ano** nebo **Ne**. Pokud tuto možnost nastavíte na **Ano**, pracovník může upravovat kód důvodu, když se zobrazí během inventury na mobilním zařízení.

> [!NOTE]
> Tlačítko **Cyklická inventura** může být povoleno na jakékoliv položce nabídky mobilního zařízení, na kterém lze provést inventuru. Příklad zahrnuje položky nabídky pro místní inventury, práci řízenou uživatelem a práci řízenou systémem.

## <a name="cycle-count-approvals"></a>Schválení cyklické inventury

Před schválením inventury uživatel může změnit kód důvodu, který je přidružen k inventuře. Po schválení inventury se zadává kód důvodu do řádků deníku inventur.

### <a name="modify-cycle-count-approvals"></a>Úprava schválení cyklické inventury

1. Vyberte **Řízení skladu** \> **Cyklická inventura** \> **Cyklická inventura práce čeká na kontrolu**.
2. Zvolte **Cyklická inventura**a pak v poli **Kód důvodu** vyberte nový kód důvodu.

### <a name="modify-the-mobile-device-menu-item-for-adjustment-in-and-adjustment-out"></a>Úprava položky nabídky mobilního zařízení pro příchozí a odchozí úpravu

1. Vyberte **Řízení skladu** \> **Nastavení** \> **Mobilní zařízení** \> **Položky nabídky mobilního zařízení** a poté vyberte **Příchozí a odchozí úpravy**.
2. Nastavte hodnotu možnosti **Použít stávající práci** na **Ne**.
3. V poli **Proces pro vytvoření práce** vyberte **Příchozí úprava**.

Následující pole budou přidána do položky nabídky mobilního zařízení, když je během procesu vytváření práce vybrána **Příchozí úprava** nebo **Odchozí úprava**:

- Výchozí kód důvodů inventury
- Zobrazit kód důvodů inventury
- Upravit kód důvodů inventury
