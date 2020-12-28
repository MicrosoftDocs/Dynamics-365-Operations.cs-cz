---
title: Platební metody v kontaktních střediscích
description: Toto téma popisuje různé platební metody, které lze použít v kontaktním středisku v aplikaci Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 03/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: MCRSalesTableOrderHistory, MCRCCAuthManagement
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 92163
ms.assetid: 8e738907-870b-466c-ab0c-07f4a4aa47f3
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: e7636f5c664634c680edf2ff9d8bae5ebb9035af
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410798"
---
# <a name="payment-methods-in-call-centers"></a>Platební metody v kontaktních střediscích

[!include [banner](includes/banner.md)]

V aplikaci Dynamics 365 Commerce zahrnuje konfigurace kanálu kontaktního střediska nastavení s názvem **Povolit dokončení objednávky**. Toto nastavení pomáhá zajistit, aby všechny objednávky, které vytvořili uživatelé kanálu, byly uvolněny ke zpracování objednávek pouze v případě, že mají předplacenou nebo předběžně autorizovánou platbu ve schválených tolerancích. Pokud je nastavení **Povolit dokončení objednávky** zapnuté, uživatelé kontaktního střediska mohou zadat platby proti prodejním objednávkám pro odběratele pomocí funkcí zpracování plateb kontaktního střediska. Pokud je nastavení vypnuto, uživatelé kontaktního střediska nemohou používat funkce zpracování plateb kontaktního střediska, ale mohou stále použít zálohy na prodejní objednávky pomocí standardních funkcí pohledávek.

Jako součást konfigurace kanálu může společnost definovat způsoby platby, které jsou povoleny pro kanál kontaktního střediska. Kanál kontaktního střediska používá stejné metody platby, které jsou definovány pro obchodní kanály.

Chcete-li nastavit způsoby platby pro kanál kontaktního střediska, přejděte na **Maloobchod a velkoobchod** \> **Kanály** \> **Kontaktní střediska** \> **Všechna kontaktní střediska** a poté v nabídce **Nastavení** zvolte možnost **Platební metody**.

Při vytváření způsobu platby existuje pět funkcí metod platby, které lze přiřadit.

| Funkce            | popis |
|---------------------|-------------|
| Normální              | Použijte funkci **Normální** na váš způsob platby při definování metod platby, jako je například hotovost nebo doklady. Při použití tohoto typu plateb na prodejní objednávku v kontaktním středisku bude ve výchozím nastavení příznak **Záloha** nastaven na **Ano**. To okamžitě zaúčtuje doklad o záloze na účet odběratele, jakmile je tato objednávka odeslána. Uživatelé mohou měnit příznak **Záloha** na **Ne**, pokud chtějí, aby platební doklad nebyl vytvořen až do zaúčtování faktury. Zálohový doklad se zaúčtuje do historie transakcí zákazníka, kde bude systematicky vyrovnán proti faktuře pro prodejní objednávku. |
| Kontrola               | Použijte funkci **Šek** při definování nástroje bankovního šeku jako metody platby. Při použití tohoto typu platby na prodejní objednávku musí uživatel zadat číslo šeku zákazníka v rámci zpracování aplikace plateb. Platby šekem se vždy považují jako zálohy, pokud jsou použity, a doklady o platbě se vytvoří okamžitě po odeslání objednávky. Tyto zálohové doklady budou systematicky vyrovnány proti fakturám, které jsou vytvořeny pro objednávku. |
| Karty               | Typy plateb kartou představují všechny typy platby, které vyžadují zadání čísla karty, které bylo definováno pro platební kartu odběratele. Příklady zahrnují kreditní karty a dárkové poukazy. Při konfiguraci těchto typů plateb je třeba použít nabídku **Nastavení karty** pro definování ID karty, která jsou přidružena k této platební metodě. V době zadání objednávky mohou uživatelé určit, zda platby kartou budou předplaceny pomocí možnosti **Záloha**, která se zobrazí na stránce zadávání plateb. Pokud nepožaduje obchod zálohové platby, je typický postup skutečné platby kredfitní kartou procesem o dvou krocích, kdy je získána autorizace v době zadání objednávky a platba je pak vyrovnána a přijata z karty zákazníka v okamžiku fakturace. Pro platby dárkovým poukazem se doporučuje zálohy, protože zůstatek dárkového poukazu byy měl být snížen okamžitě, aby odběratel nemohl použít stejnou hodnotu někde jinde. |
| Zákazník            | Funkce **Odběratel** u způsobu platby předpokládá, že platba bude použita na limit kreditu odběratele nebo bude převedena „na účet“. V aplikaci Commerce může být odběrateli přiřazen limit úvěru, který lze ověřit v době zadání objednávky. Platby, které se provádí pomocí platební metody navázané na funkci **Odběratel** vytváří závazky proti účtu odběratele. Při fakturaci prodejní objednávky se poté zobrazí splatný zůstatek. V těchto situacích odběratelé obvykle posílají platbu podle stanovených podmínek. Popřípadě lze použít předchozí otevřený kreditní doklad na účtu odběratele pro vyrovnání splatného zůstatku. povšimněte si, že i když definujete tento způsob platby, nezobrazí se mezi možnostmi výběru platby v zadávání objednávek kontaktníhoho střediska, pokud není příznak **Povolit na účet** nastaven na záznamu odběratele pro odběratele, se kterým pracujete. Tento příznak se nachází na kartě **Výchozí nastavení plateb** záznamu odběratele. |
| Úhrada – odebrat/plovoucí | Funkce **Úhrada – odebrat/plovoucí** se nepoužívá v kontaktním středisku. Je použitelná jen při definování metody platby, kterou používá aplikace pokladního místa v kanálu obchodu. |

Když jsou metody platby vytvořeny, měly by být navázány na hlavní knihu nebo bankovní účet. Pokud tento krok vynecháte, uživatelé obdrží chyby, když se pokusí uložit typ platby.

## <a name="refund-payment-methods"></a>Způsob refundace platby

Pro scénáře zpracování refundace používá kontaktní středisko také některé z metod platby, které se definují v modulu Pohledávky. Chcete-li konfigurovat tyto metody plateb, přejděte na **Maloobchod a velkoobchod** \> **Nastavení kanálu** \> **Nastavení kontaktního střediska** \> **Metody refundace kontaktního střediska**. Je nutné dokončit tuto konfigurace pro zpracování šeků refundace odběratelům. Například platí-li odběratel původně objednávku hotovostí nebo šekem, uživatel může chtít odeslat odběrateli šek refundace prostřednictvím pohledávek. Typy plateb hotovostí a šekem v kontaktním středisku musí být v takovém případě namapovány na správnou metodu platby v modulu Pohledávky, aby se zajistilo správné zpracování refundace.

Dále, pokud uživatel zpracovává vratku jako uživatel kontaktního střediska v aplikaci Commerce, ale nemůže navázat vratku na původní prodej, musí být definována platební metoda **Vrácení** v parametrech kontaktního střediska. Přejděte na **Maloobchod a velkoobchod** \> **Nastavení kanálu** \> **Nastavení kontaktního střediska** \> **Parametry kontaktního střediska** a poté na kartě **RMA/vratky** v poli **Způsob platby** nadefinujte způsob platby. Metoda platby bude metodou platby použitou pro refundace. Obvykle bude definována buď jako metodu šeku nebo jako metoda účtu odběratele.
