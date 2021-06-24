---
title: Nastavení zaúčtování správy rabatu
description: Toto téma Popisuje, jak nastavit účetní profily. Účetní profily se používají k určení položek účtování pro řádky výpočtu správy rabatů.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 808080d9e84c4af1b061d5a4ce76d5fa309e66f7
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216736"
---
# <a name="rebate-management-posting-setup"></a>Nastavení zaúčtování správy rabatu

[!include [banner](../includes/banner.md)]

Účetní profily správy rabatů se používají k určení položek účtování pro řádky výpočtu správy rabatů. Když je v záhlaví nabídky vybrán účetní profil, použije se na všechny řádky nabídky.

Tato funkce funguje napříč společnostmi (právnickými osobami). Můžete určit společnost, pro kterou budou časově rozlišeny dodávky a kterou budou zaplaceny nároky. Můžete také nastavit různé debetní účty dodávek a kreditní účty odpisů podle zdrojové účetní společnosti.

Chcete-li nastavit účetní profily správy rabatu pro zákazníky a dodavatele, přejděte na **Správa rabatů \> Nastavení účtování správy rabatů \> Účetní profily správy rabatů**. Stránka **Účetní profily správy rabatů** obsahuje podokno se seznamem, které zobrazuje všechny vaše stávající profily. Tlačítka v podokně akcí můžete přidat profily do seznamu nebo je odstranit.

Zbývající části tohoto tématu Popisují, jak použít dostupná pole při vytváření nebo úpravách profilu.

## <a name="posting-profile-header"></a>Záhlaví účetního profilu

Následující tabulka Popisuje nastavení, která jsou k dispozici v části záhlaví každého účetního profilu správy rabatů.

| Pole | Popis |
|---|---|
| Účetní profil | Zadejte jedinečný název profilu. |
| Popis | Zadejte Popis profilu. |
| Modul | Vyberte typ rabatů a autorských poplatků, s nimiž je profil spojen (*Zákazník* nebo *Dodavatel*). |
| Typ | Vyberte typ profilu (*Rabat* nebo *Autorský poplatek*). |
| Typ platby | <p>Toto pole určuje formát zaúčtovaného výstupu rabatu.<p><p>Když je pole **Typ** nastaveno na *Rabat*, jsou k dispozici následující hodnoty:</p><ul><li>*Platba pomocí závazků* - Když zaúčtujete zákaznický rabat, vytvoří se faktura dodavatele pro dodavatele úhrady, která je nastavena na zákazníka rabatu. Když zaúčtujete rabat dodavatele, vytvoří se faktura dodavatele pro účet dodavatele rabatu.</li><li>*Odpočty zákazníků* - Když zaúčtujete rabat, vytvoří se deník odpočtu zákazníka pro zákazníka rabatu.</li><li>*Odpočty zákazníka daňové faktury* - Když zaúčtujete rabat, vytvoří se volná faktura pro zákazníka rabatu.</li><li>*Obchodní výdaje* - Když zaúčtujete rabat, vytvoří se deník odpočtu zákazníka pro zákazníka rabatu.</li><li>*Vykazování* - Když zaúčtujete rabat, vytvoří se deník odpočtu zákazníka pro zákazníka rabatu.</li></ul><p>Když je pole **Typ** nastaveno na *Autorský poplatek*, jsou k dispozici následující hodnoty:</p><ul><li>*Platba pomocí závazků* - Když zaúčtujete rabat, vytvoří se faktura dodavatele pro účet dodavatele rabatu.</li><li>*Vykazování* - Když zaúčtujete rabat, vytvoří se faktura dodavatele pro účet dodavatele rabatu.</li></ul><p>Další informace naleznete v následující části [Typy plateb](#payment-types). |
| Společnost | Zvolte společnost (právnickou osobu), pro kterou budou časově rozlišeny dodávky a kterou budou zaplaceny nároky. |

### <a name="payment-types"></a>Typy plateb

Následující tabulka shrnuje, jak různá nastavení pole **Typ platby** ovlivní, kde jsou zaúčtovány platby. Platby lze zaúčtovat na zákaznický účet, účet dodavatele nebo na účet úhrady, v závislosti na cílové transakci a typu rabatu.

| Typ platby | Typ cílové transakce | Typ rabatu | Platba na (fakturační účet) |
|---|---|---|---|
| Platba pomocí závazků | Deník faktur dodavatele | Rabat odběratele | Účet dodavatele úhrady zákazníka |
| Platba pomocí závazků | Deník faktur dodavatele | Autorský poplatek zákazníka | Účet dodavatele |
| Platba pomocí závazků | Deník faktur dodavatele | Rabat dodavatele | Účet dodavatele |
| Srážky u odběratele | Denní deník | Rabat odběratele | Účet odběratele |
| Odpočty zákazníků daňové faktury | Volné faktury | Rabat odběratele | Účet odběratele |
| Obchodní výdaje | Denní deník | Rabat odběratele | Účet odběratele |
| Vykazování | Denní deník | Rabat odběratele | Účet odběratele |
| Vykazování | Deník faktur dodavatele | Autorský poplatek zákazníka | Účet dodavatele |
| Vykazování | Deník faktur dodavatele | Rabat dodavatele | Účet dodavatele |

> [!NOTE]
> Při nastavování [nabídek správy rabatu](rebate-management-deals.md) zvažte následující body:
>
> - Pro nabídky, kde je pole **Odsouhlasit podle** je nastaveno na *Nabídka*, nemůžete během zaúčtování použít dynamický účet nabídky. Musíte použít určený účet zákazníka nebo dodavatele.
> - Pro nabídky, kde je pole **Odsouhlasit podle** nastaveno na *Řádek*, můžete použít účetní profil, který kompenzuje dynamický účet nabídky na řádku nabídky, protože zákazník je nastaven podle řádku nabídky.

## <a name="posting-fasttab"></a>Záložka s náhledem Účtování

Následující tabulka popisuje pole, která jsou k dispozici na záložce s náhledem **Účtování** každého účetního profilu správy rabatů.

| Pole | Popis |
|---|---|
| Typ strany Dal | Vyberte, zda chcete připsat kredit na účet hlavní knihy nebo na zákazníka či dodavatele. |
| Dal účet | Účet, na který jsou zaúčtovány částky kreditu, při vytvoření dodávek rabatu. Tento účet bude také použit jako debetní účet, když je rabat zaúčtován pro kredit zákazníka. |
| Název deníku<br>(V části **Dodávka**) | Vyberte název deníku, který se má použít k zaznamenání zaúčtované dodávky. |
| Typ | Vyberte, zda chcete zaúčtovat rabat na účet hlavní knihy nebo na zákazníka či dodavatele. Pokud je pole **Typ platby** v záhlaví nastaveno na *Odpočty zákazníků daňové faktury*, toto pole je nastaveno na *Zákazník/dodavatel*. |
| Použití zdroje účtu | <p>Vyberte jednu z následujících hodnot:</p><ul><li>*Žádný* - Pokud vyberete tuto hodnotu, musíte zadat účet v poli **Účet rabatu**.</li><li>*Účet nabídky* - Použijte účet zákazníka nebo dodavatele uvedený na řádku rabatu. Tuto hodnotu můžete vybrat pouze u nabídek, kde je pole **Odsouhlasit podle** nastaveno na *Řádek* a řádky nabídky, kde je pole **Kód účtu** nastaveno na *Tabulka*. To se nevztahuje na účetní profily autroských poplatků zákazníků.</li></ul> |
| Účet rabatu | Účet, na který budou skutečné náklady rabatu zaúčtovány. |
| Název deníku<br>(V sekce **Správa rabatu**) | Vyberte název deníku, který se má použít k zaúčtování dobropisu pro částku rabatu zákazníkovi. Toto pole není k dispozici, pokud je pole **Typ platby** v záhlaví nastaveno na *Odpočty zákazníků daňové faktury*. |
| Skupina DPH zboží | Uveďte, zda je rabat zdanitelný. |
| Název deníku<br>(V sekci **Odpis**) | Pokud se zaúčtovaný rabat nerovná dodávce, může být rozdíl odepsán. Vyberte název deníku, který se má použít k zaznamenání zaúčtovaného odpisu. |

## <a name="posting-by-company-fasttab"></a>Záložka s náhledem Zaúčtování podle společnosti

Záložka s náhledem **Zaúčtování podle společnosti** každého účetního profilu správy rabatu vám umožní určit účet pro zaúčtování, který používá každá společnost (právnická osoba) v mřížce.

Tlačítka na panelu nástrojů používejte k přidání společností do mřížky a jejich odstranění. Pokaždé, když přidáte řádek do mřížky, použijte pole **Společnost** pro určení právnické osoby pro daný řádek. Pole **Název** se poté nastaví automaticky.

Vyberte řádek pro každou společnost a poté pomocí polí pod mřížkou zadejte následující informace:

- **Typ debetu** – Vyberte, zda chcete připsat debet na účet hlavní knihy nebo na zákazníka či dodavatele.
- **Účet debetu** - Zadejte účet, na který je zaúčtována částka debetu, když jsou vytvořeny dodávky.
- **Hlavní účet** - Vyberte hlavní účet pro odpisy.
