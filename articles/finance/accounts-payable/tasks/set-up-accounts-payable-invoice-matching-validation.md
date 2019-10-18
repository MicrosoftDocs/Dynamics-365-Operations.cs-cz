---
title: Nastavení ověřování párování faktur závazků
description: Toto téma obsahuje informace o způsobu nastavení ověření párování faktur závazků.
author: abruer
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b048c49de7357ec1b5cbf36dd4f22a5d3efd443b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189400"
---
# <a name="set-up-accounts-payable-invoice-matching-validation"></a>Nastavení ověřování párování faktur závazků

[!include [task guide banner](../../includes/task-guide-banner.md)]

Před prvním krokem ověřte, že je vybraný konfigurační klíč Párování faktur. Pokud vaše právnická osoba sleduje výdaje, jako jsou například dopravné, pomocí nákladů, ujistěte se, že je vybrán konfigurační klíč Poplatky.  Párování faktur závazků je procesem párování informací na faktuře dodavatele, nákupní objednávce a příjemce produktu. Rozdíly mezi těmito dokumenty jsou označovány jako odlišnosti v párování. Odlišnosti v párování se porovnávají s odchylkami, které jsou zadány. Pokud odchylka párování překračuje procento nebo částku tolerance, zobrazí se odpovídající ikona na stránce **Faktura dodavatele** a na stránce **Podrobnosti o párování faktur**.

## <a name="determine-which-invoice-matching-validation-to-use"></a>Určení toho, jaké ověření párování faktur se má použít
K dispozici jsou čtyři různé typy ověření párování. 

- **Párování na úrovní řádků** – nejběžnější typ párování je párování řádků. Párování na úrovni řádku může být dvoucestné nebo třícestné. Výchozí párování na úrovni řádku lze určit pro právnickou osobu na stránce **Parametry závazků**. Dvoucestné párování srovnává jednotkovou cenu na faktuře s jednotkovou cenou na nákupní objednávce. Třícestné párování navíc porovnává fakturované množství se spárovaným množstvím příjemky produktu.
- **Párování součtů faktur** – párování celkových částek na faktuře s celkovými částkami na nákupní objednávce. Tento typ párování faktur zahrnuje nejmenší množství podrobností, takže ho můžete použít k vytvoření ovládacích prvků, které zaměstnancům minimalizují čas potřebný ke kontrole informací o párování faktur. Je porovnáno šest součtů, včetně mezisoučtu, celkové slevy, nákladů, DPH, zaokrouhlení a fakturované částky. Systém ověří, zda se kterákoli z těchto hodnot na faktuře liší od očekávaných částek o více než přijatelnou odchylku.
- **Párování nákladů**– páruje informace o nákladech (částky) na faktuře s informacemi o nákladech (částky) na nákupní objednávce.
- **Celkové ceny pro párování položky řádku** – tento typ párování je užitečný pro společnosti, které obvykle přijímají více faktur pro jeden řádek nákupní objednávky. Pokud obvykle obdržíte pouze jednu fakturu na řádek nákupní objednávky, není tento typ párování nutný. Toto párování vyžaduje, aby bylo povoleno dvoucestné nebo třícestné párování, a slouží jako ověření nepřekročení čisté částky, které je založeno na procentech tolerance a částkách.  Tento typ párování porovnává informace o ceně pro čistou částku na každém řádku faktury a všechny čekající a dříve zaúčtované řádky faktury s čistou částkou na odpovídajícím řádku nákupní objednávky. Čistá částka je určována podle tohoto vzorce: (jednotková cena * množství na řádku) + náklady na řádku − slevy na řádku. Při párování celkové ceny podle procent, systém porovnává hodnoty pomocí měny transakce. Při párování celkové ceny podle částky, systém porovnává hodnoty pomocí zúčtovací měny.

## <a name="set-up-parameters-to-enable-invoice-matching-validation"></a>Nastavení parametrů pro povolení ověření párování faktur
1. Přejděte do nabídky **Závazky > Nastavení > Parametry závazků**
2. Zvolte kartu **Ověření faktury**.
3. Zaškrtněte políčko **Povolit ověření párování faktur** nebo jeho zaškrtnutí zrušte.
    * Vyberte, zda má být před zaúčtováním faktury obsahující odchylky párování faktur vyžadováno schválení. Pokud zde nastavíte **Povolit s varováním**, vizuální označení budou zobrazeny v případě, že odchylka při párování faktur bude vyšší než tolerance. I přesto však bude možné zaúčtovat fakturu. Pokud chcete použít workflow společně s ověřením párování faktur, ujistěte se, v poli **Zaúčtovat fakturu s odchylkami** je vybrána hodnota **Povolit s varováním**, abyste nemuseli proces schvalovat vícekrát.  
    * V poli **Automaticky aktualizovat stav záhlaví faktury** určete, zda se párování provede automaticky při zadání dat faktury pomocí systému. Doporučená nastaveny je hodnota **Ano**, pokud nemáte obavy o výkon vstupních dat. Zakázání automatických aktualizací umožní systému pracovat rychleji, protože ověřování párování faktur bude při zadávání dat vynecháno. Pokud je nastavena hodnota **Ne**, úředník pro zadání dat bude muset ručně aktualizovat stav párování faktury, aby mohl vidět výsledky ověření párování faktur.  
4. Nastavte **Párování součtu faktur**.
5. Zvolte nebo vymažte zaškrtávací pole **Párování součtu faktur** tak, aby skutečné součty faktur odpovídaly očekávaným součtům.
    * Určete, zda bude zobrazena ikona, je-li odchylka párování faktur vyšší než tolerance. Můžete vybrat zobrazení ikony, když je kladný rozdíl vyšší než tolerance nebo pokud kladný nebo záporný rozdíl je vyšší než tolerance.  
    * Například tolerance je 5 procent a celková částka faktury v nákupní objednávce je 100,00. Proto se bude ikona párování cen zobrazena, pokud celková částka faktury na faktuře překročí cenu 105,00. Pokud vyberete volbu **Pokud vyšší nebo nižší než tolerance**, bude ikona zobrazena také v případě, že částka faktury je nižší než 95,00.  
6. Do pole **Tolerance součtu faktur v procentech** zadejte přijatelnou procentuální odchylku. Tato hodnota představuje výchozí hodnotu pro společnost. Tuto hodnotu lze přepsat pro určité dodavatele pomocí stránky **Tolerance součtu faktur**. Informace o tom, jak přepsat procento tolerance součtu faktur pro specifického dodavatele, naleznete v části „Nastavení tolerance párování celkových faktur pro dodavatele“ dále v tomto tématu.
7. Nastavte **Párování ceny a množství**.
8. V poli **Zásady párování řádků** vyberte hodnotu, která má být použita jako výchozí zásada pro právnickou osobu, se kterou pracujete. Možnost **Nevyžadovaná** znamená, že nejsou zapotřebí ověřování ceny na jednotlivých řádcích faktury podle ceny nákupní objednávky nebo množství na faktuře na dodacím listu. **Dvoucestné párování** znamená, že je požadováno ověřovací řádků faktury, ale při ověření jsou zahrnuty pouze nákupní objednávky a dokumenty s fakturou dodavatele. Příjemka produktu není promítnuta do ověření párování. **Třícestné párování** znamená, že čistá jednotková cena na faktuře se bude porovnávat s čistou jednotkovou cenou nákupní objednávky, a odpovídající množství v příjemce produktu se bude porovnávat s množstvím ve faktuře.
9. Chcete-li povolit různé úrovně párování pro zboží, dodavatele, kombinaci dodavatele a zboží nebo řádek nákupní objednávky, vyberte hodnotu v poli **Povolit přepsání zásad párování**. Zásady párování řádku právnické osoby lze obejít pro určitého dodavatele, zboží nebo kombinaci dodavatele a zboží na stránce **Zásady párování**.
    * Při použití zásady párování typu Dvoucestné párování nebo Třícestné párování, můžete nastavit procentuální hodnoty tolerance ceny pro právnickou osobu, položky a dodavatele na stránce **Tolerance ceny položky**. Výchozí tolerance ceny právnické osoby bude nastavena na nula procent pro dvoucestné a třícestné párování. Při porovnání faktur dodavatelů s informacemi na nákupních objednávkách vyhledá se vhodná procentuální hodnota tolerance cen.   
10. Chcete-li spárovat celkové ceny pro řádkové položky na fakturách, vyberte hodnotu v poli **Párování celkových cen**. Tento typ párování je užitečný, když dodavatel odešle více faktur pro stejný řádek nákupní objednávky. Můžete porovnat informace o ceně pro čistou částku na každém řádku faktury a všechny čekající a dříve zaúčtované řádky faktury s čistou částkou na odpovídajícím řádku nákupní objednávky.  Možnosti zahrnují **Žádnái**, **Procento**, **Částka**, nebo **Procento a částka**.
11. V poli **Procento tolerance celkové nákupní ceny** zadejte procentuální hodnotu odchylky, kterou přijmete. Toto pole je k dispozici, když je **Párování celkových cen** nastaveno na **Procento** nebo **Procento a částka**.
12. Do pole **Tolerance celkové nákupní ceny** zadejte částku v zúčtovací měně. Toto pole je k dispozici, když je **Párování celkových cen** nastaveno na **Částka** nebo **Procento a částka**.
13. V poli **Zobrazit ikonu párování celkových cen** určete, kdy bude zobrazena ikona, je-li odchylka párování faktur vyšší než tolerance čisté jednotkové ceny. Ikonu lze zobrazit, když je kladný rozdíl vyšší než tolerance nebo pokud kladný nebo záporný rozdíl je vyšší než tolerance.
Například tolerance je 5 procent a celková řádková cena v nákupní objednávce je 10,00. Proto se bude ikona párování cen zobrazena, pokud celková řádková cena na faktuře překročí cenu 10,50. Pokud vyberete volbu **Pokud vyšší nebo nižší než tolerance**, bude ikona zobrazena také v případě, že součet cen řádků na faktuře je nižší než 9,50.
13. Nastavte Párování nákladů.
14. Aby odpovídaly skutečným nákladům s očekávanými náklady na základě informací o nákupní objednávce, zaškrtněte políčko **Porovnání nákladů**.

## <a name="set-up-unit-price-tolerance-percentages"></a>Nastavení procentuálních hodnot tolerance jednotkových cen
Chcete-li definovat povolená procenta tolerance cen, přejděte na **Závazky > Nastavení > Nastavení párování faktur >Tolerance ceny**. Při použití zásady párování typu dvoucestné párování nebo třícestné párování, můžete nastavit procentuální hodnoty tolerance ceny pro právnickou osobu, položky a dodavatele. Při porovnání faktur dodavatelů s informacemi na nákupních objednávkách vyhledá se vhodná procentuální hodnota tolerance cen. Toto je výchozí pořadí vyhledávání:
* Tabulka/tabulka
* Tabulka/skupina
* Tabulka/vše
* Skupina/tabulka
* Skupina/skupina
* Skupina/vše
* Vše/tabulka
* Vše/skupina
* Vše/vše

Výchozí tolerance ceny právnické osoby je 0 procent a tato tolerance ceny je použita pro všechny položky a všechny účty (Vše, Vše). Záznam výchozí tolerance ceny právnické osoby nelze odstranit.

Ve výchozím nastavení jsou povoleny záporné odchylky cen. Záporné číslo však jako procentuální hodnotu tolerance cen položek není možné zadat. Chcete-li sledovat záporné procento tolerance ceny, vyberte možnost **Pokud vyšší nebo nižší než tolerance** v poli **Zobrazit ikonu párování jednotkové ceny** na stránce **Parametry závazků**. Poté zadejte procenta tolerance ceny na stránce **Tolerance ceny**.

## <a name="set-up-matching-policy-override"></a>Nastavení přepsání zásad párování

Chcete-li definovat výchozí zadání pro pole zásad párování pro řádky ve formulář nákupní objednávky, přejděte na > **Závazky > Nastavení > Nastavení párování faktur > Zásady párování**. Toto je volitelné nastavení. Tento formulář slouží k nastavení dvoucestného nebo třícestného párování pro položky, dodavatele nebo kombinace položek a dodavatelů. Tato zadání vám umožňují definovat podrobnější zásady párování, než jsou zásady párování právnických osob definované na stránce **Parametry závazků**. Výchozí zásada párování řádků právnické osoby bude použita pro všechny položky a dodavatele s výjimkou těch, pro které je na této stránce určena jiná zásada párování řádků.

Na této stránce vyberte **Úroveň zásad párování**. Zvolte úroveň v hierarchii zásad párování, pro kterou chcete nastavit zásady párování řádku.

- **Položka a dodavatel** – zadejte zásad párování pro konkrétní položky, které jsou nakoupeny od určitých dodavatelů.
- **Položka** – stanovte zásadu párování pro konkrétní položky, které jsou zakoupeny od libovolného dodavatele, s výjimkou těch, které jsou zadány na úrovni položky a dodavatele.
- **Dodavatel** – stanovte zásadu párování pro všechny položky, které jsou zakoupeny od konkrétního dodavatele, s výjimkou těch, které jsou zadány na úrovních položky a dodavatele a položky.
  
Následující hierarchie slouží k určení zásady párování, která se používá:
  *  Položka a dodavatel
  *  Zboží
  *  Dodavatel
  *  Právnická osoba
  
## <a name="set-up-invoice-totals-matching-tolerance-for-vendors"></a>Nastavení tolerance párování součtů faktur pro dodavatele

Chcete-li určit tolerance specifické pro dodavatele pro párování součtů faktur, přejděte na **Závazky > Nastavení > Nastavení párování faktur > Tolerance součtu faktur**. Výpočet párování používá procento tolerance součtu faktur z účtu dodavatele, který je určen jako účet objednávky na faktuře dodavatele. Pokud účet dodavatele nemá zadané procento tolerance pro součty faktur, použije se procento tolerance součtu faktur zadané pro právnickou osobu na stránce **Parametry závazků**.

1. Chcete-li určit tolerance pro jednotlivé dodavatele, kteří přepíší výchozí tolerance, zvolte **Účet dodavatele**.
2. Zadejte procento odchylky přijatelné pro tohoto dodavatele.
