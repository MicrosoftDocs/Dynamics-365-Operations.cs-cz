---
title: "Uzavřít zásoby"
description: "Jako součást procesu vyrovnání výdejových transakcí s příjmovými transakcemi můžete rovněž aktualizovat hlavní knihu tak, aby došlo k promítnutí provedených úprav."
author: AndersGirke
manager: AnnBe
ms.date: 10/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventClosing
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 61973
ms.assetid: c210c882-6849-4704-b78c-a777dd6cfdb6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: dfb6b9c2f4bad95c165a8d8a1e888e7a67e66c69
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="inventory-close"></a>Uzavřít zásoby

[!include [banner](../includes/banner.md)]

Jako součást procesu vyrovnání výdejových transakcí s příjmovými transakcemi můžete rovněž aktualizovat hlavní knihu tak, aby došlo k promítnutí provedených úprav.

Proces uzávěrky skladu v aplikaci vyrovná výdejové transakce příjmovými transakcemi podle metody oceňování zásob, která je vybraná ve skupině modelu zboží. Jako součást procesu vyrovnání lze zadat, že má být aktualizována hlavní kniha, aby odrážela úpravy, které byly provedeny. Nicméně až do spuštění uzávěrky skladu nebo přepočtu se používá při účtování výdejových transakcí vypočtená průběžná průměrná nákladová cena. 

Po uzávěrce skladu již nebude možné zaúčtovat do období před nastaveným datem uzávěrky skladu, pokud neprovedete zpětnou dokončenou závěrku skladu. Pokud je například uzávěrka skladu spuštěná pro období končící 31. ledna, nemůžete zaúčtovávat transakce, jejichž datum předchází 31. lednu. 

Zboží ve skladu je přiřazeno jednomu ze dvou typů zásob: zboží nebo služba. Uzávěrka skladu provede stejné funkce u obou typů. Avšak u položek typu služba uzávěrka skladu stále slouží k úhradě výdejů na příjemkách. 

Četnost spouštění procesu uzávěrky skladu se liší pro každou společnost. Objem transakcí však má pomoci zjistit, jak často je vhodné spuštění uzávěrky skladu. Obecně platí, že většina společností spouští uzávěrku skladu jako součást závěrky a odsouhlasení na konci měsíce.

## <a name="inventory-recalculation-and-the-general-ledger"></a>Přepočet skladu a hlavní kniha
Jsou-li v průběhu měsíce nutné opravy zásob a hlavní knihy, můžete místo uzávěrky skladu spustit přepočet zásob. Do přepočtu zásob se promítnou opravy, ale nebude provedeno vyrovnání skladových transakcí. 

Při přepočtu skladu jsou upraveny zásoby na skladě a skladové transakce a proběhnou přepočty zásob a uzávěrky skladu. Tyto úkoly mají vliv na jakýkoli účet hlavní knihy, který je spojený s původní skladovou transakcí. 

**Příklad** 

Když vytvoříte nákupní objednávku z prodejní objednávky, aktualizují se účty hlavní knihy, které jsou použité pro původní prodejní objednávku. I v případě, že se od zaúčtování prodejní objednávky změnily účty hlavní knihy pro skupinu položek přiřazenou k dané položce a došlo k vytvoření částky úpravy pomocí přepočtu skladu, částka úpravy bude zaúčtována na původní účty hlavní knihy. Upravená částka není zaúčtována na účtech hlavní knihy, které jsou přiřazeny k položce. 

Po dokončení aktualizace můžete zkontrolovat doklad hlavní knihy, který byl zaúčtován kvůli některému z těchto úkolů.

1.  Na kartě **Přehled** na stránce **Závěrka a oprava** vyberte aktualizace ke kontrole.
2.  Klikněte na tlačítko **Podrobnosti** a poté vyberte možnost **Doklad**.

## <a name="effects-of-the-inventory-close-process-on-the-general-ledger"></a>Účinky procesu uzávěrky skladu na hlavní knihu
Některé úkoly, které lze provést pomocí stránky **Závěrka a oprava**, způsobí aktualizaci hlavní knihy. Hlavní kniha se například aktualizuje, pokud provedete úpravy množství na skladě, úpravy skladových transakcí, spouštění přepočtu skladu nebo spouštění uzávěrky skladu. 

Aktualizovány budou účty hlavní knihy, které jsou spojené s původní skladovou transakcí. Pokud je například prodejní objednávka vyrovnána s nákupní objednávkou, budou upraveny účty hlavní knihy, které byly použity pro původní prodejní objednávku. Toto chování platí i v případě, že účty hlavní knihy pro skupiny položek přiřazených dané položce se změnily po zaúčtování prodejní objednávky. Po uzávěrce skladu dojde k vytvoření částky vyrovnání, částka vyrovnání bude přesto zaúčtována k původním účtům hlavní knihy, nikoli na nové účty hlavní knihy přiřazených k dané položce. Hlavní kniha může být aktualizována také stornováním uzávěrka skladu. 

**Poznámky:**

-   Uzávěrka skladu není vyžadována při použití oceňovací metody Standardní náklady.
-   Před spuštěním postupu uzávěrky se zobrazí seznam položek, které nelze vyrovnat v průběhu aktualizace.
-   Doporučujeme spustit uzávěrku skladu v době minimálního provozu, což umožní rovnoměrné vytížení výpočetních zdrojů.

## <a name="the-inventory-close-log"></a> Protokol uzávěrky skladu
Po dokončení procesu uzávěrky skladu se může objevit zpráva ve středisku zpráv o nesprávné hodnotě jednotkové nákladové ceny, protože transakci nebylo možné úplně vyrovnat. 

Před zobrazením této zprávy systém nahlásí číslo položky a ovlivněnou transakci. Tato zpráva informuje o tom, že částka nákladů použitá pro tuto transakci nebyla jako důsledek uzávěrky skladu aktualizována. Tato zpráva se zobrazí, pokud transakce typu „výdej“ nelze vyrovnat. 

Během procesu uzávěrky skladu systém provede kontrolu pro každou finanční dimenzi, aby se zjistilo, zda do specifikovaného data uzávěrky existuje více výdejů než příjmů. Tento typ nevyrovnanosti může nastat tehdy, když skladová transakce z nákupní objednávky není plně zaúčtována finančně, protože faktura dodavatele ještě nebyla dodána, nebo protože položka kusovníku zahrnutá do výroby na vyšší úrovni není finančně zaúčtována. (Nejsou ještě vypočteny náklady na dílčí výrobu). Pokud k tomu dojde, následná uzávěrka neopraví všechny výdeje na správnou nákladovou cenu, protože není k dispozici dostatek informací o příjmu. 

Před každým spuštěním uzávěrky systém určí, zda protokol, který obsahuje upozornění, je uložen a lze jej zobrazit. 

Pokud jste zdrojem velkého počtu varování, je doporučeno provést následující akce:

-   Finanční aktualizace příjmů.
-   Posuňte datum uzávěrky.
-   Přehodnoťte své obchodní postupy.

V některých případech nemusí být možné provádět žádné akce pro uvedená upozornění. Když se například označení použije u označené nákupní objednávky, která má finanční datum po datu uzávěrky, nelze datum uzávěrky změnit.

## <a name="reversing-a-completed-inventory-close"></a>Zrušení dokončené uzávěrky skladu
V některých případech je nutné zrušit dokončenou uzávěrku skladu a vrátit vyrovnání do původního stavu před provedením úprav. Při zrušení dokončené uzávěrky skladu budou zásoby také znovu otevřeny, aby bylo možné účtovat do příslušného období, které pokrývá uzávěrku skladu. Související změny také mohou být udělány v hlavní knize. Po dokončení množství úprav můžete spustit znovu uzávěrku skladu pro období, ve kterém pracujete. 

**Poznámka:** Znovu otevřít lze pouze poslední zásoby období, které bylo ukončeno. Pokud chcete stornovat předchozí skladové uzávěrky, je nutné stornovat postupně každou následnou skladovou uzávěrku, počínaje poslední uzávěrkou.




