---
title: "Uzavřít zásoby"
description: "Jako součást procesu vyrovnání výdejových transakcí s příjmovými transakcemi můžete rovněž aktualizovat hlavní knihu tak, aby došlo k promítnutí provedených úprav."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-03-08 15 - 56 - 00
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventClosing
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 61973
ms.assetid: c210c882-6849-4704-b78c-a777dd6cfdb6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 4e8de5c43f9e309787e4490586c1eac3858fb9fc
ms.lasthandoff: 03/29/2017


---

# <a name="inventory-close"></a>Uzavřít zásoby

Jako součást procesu vyrovnání výdejových transakcí s příjmovými transakcemi můžete rovněž aktualizovat hlavní knihu tak, aby došlo k promítnutí provedených úprav.

Zavřít soupisu vyrovná výdejových transakcí příjmové transakce, založené na metodě ocenění zásob vybrané v skupiny modelů položky zboží. Jako součást procesu vyrovnání lze zadat, že má být aktualizována hlavní kniha, aby odrážela úpravy, které byly provedeny. Nicméně až do spuštění uzávěrky skladu nebo přepočtu se používá při účtování výdejových transakcí vypočtená průběžná průměrná nákladová cena. Po uzávěrce skladu již nebude možné zaúčtovat do období před nastaveným datem uzávěrky skladu, pokud neprovedete zpětnou dokončenou závěrku skladu. Například spuštění zavřít skladové období, které končí dnem 31 nelze zaúčtovat transakce, které mají datum, která je starší než dne 31. Jeden ze dvou typů zásob jsou přiřazeny položky ve skladu: zboží nebo služby. Uzávěrka skladu provede stejné funkce u obou typů. Avšak u položek typu služba uzávěrka skladu stále slouží k úhradě výdejů na příjemkách. Četnost spouštění procesu uzávěrky skladu se liší pro každou společnost. Objem transakcí však má pomoci zjistit, jak často je vhodné spuštění uzávěrky skladu. Obecně platí, že většina společností spouští uzávěrku skladu jako součást závěrky a odsouhlasení na konci měsíce.

## <a name="inventory-recalculation-and-the-general-ledger"></a>Přepočet skladu a hlavní kniha
Jsou-li v průběhu měsíce nutné opravy zásob a hlavní knihy, můžete místo uzávěrky skladu spustit přepočet zásob. Do přepočtu zásob se promítnou opravy, ale nebude provedeno vyrovnání skladových transakcí. Při přepočtu skladu jsou upraveny zásoby na skladě a skladové transakce a proběhnou přepočty zásob a uzávěrky skladu. Tyto úkoly mají vliv na jakýkoli účet hlavní knihy, který je spojený s původní skladovou transakcí. **Příklad**: Když vytvoříte nákupní objednávku z prodejní objednávky, aktualizují se účty hlavní knihy, které jsou použité pro původní prodejní objednávku. I v případě, že se od zaúčtování prodejní objednávky změnily účty hlavní knihy pro skupinu položek přiřazenou k dané položce a došlo k vytvoření částky úpravy pomocí přepočtu skladu, částka úpravy bude zaúčtována na původní účty hlavní knihy. Upravená částka není zaúčtována na účtech hlavní knihy, které jsou přiřazeny k položce. Po dokončení aktualizace můžete zkontrolovat doklad hlavní knihy, který byl zaúčtován kvůli některému z těchto úkolů.

1.  Na kartě **Přehled** na stránce **Závěrka a oprava** vyberte aktualizace ke kontrole.
2.  Klikněte na tlačítko **Podrobnosti** a poté vyberte možnost **Doklad**.

## <a name="effects-of-the-inventory-close-process-on-the-general-ledger"></a>Účinky procesu uzávěrky skladu na hlavní knihu
Některé úkoly, které lze provést pomocí stránky **Závěrka a oprava**, způsobí aktualizaci hlavní knihy. Hlavní kniha se například aktualizuje, pokud provedete úpravy množství na skladě, úpravy skladových transakcí, spouštění přepočtu skladu nebo spouštění uzávěrky skladu. Aktualizovány budou účty hlavní knihy, které jsou spojené s původní skladovou transakcí. Pokud je například prodejní objednávka vyrovnána s nákupní objednávkou, budou upraveny účty hlavní knihy, které byly použity pro původní prodejní objednávku. Toto chování platí i v případě, že účty hlavní knihy pro skupiny položek přiřazených dané položce se změnily po zaúčtování prodejní objednávky. Po uzávěrce skladu dojde k vytvoření částky vyrovnání, částka vyrovnání bude přesto zaúčtována k původním účtům hlavní knihy, nikoli na nové účty hlavní knihy přiřazených k dané položce. Hlavní kniha může být aktualizována také stornováním uzávěrka skladu. **Poznámky:**

-   Uzávěrka skladu není vyžadována při použití oceňovací metody Standardní náklady.
-   Před spuštěním postupu uzávěrky se zobrazí seznam položek, které nelze vyrovnat v průběhu aktualizace.
-   Doporučujeme spustit uzávěrku skladu v době minimálního provozu, což umožní rovnoměrné vytížení výpočetních zdrojů.

## <a name="the-inventory-close-log"></a> Protokol uzávěrky skladu
Po dokončení procesu uzávěrky skladu se může objevit zpráva ve středisku zpráv o nesprávné hodnotě jednotkové nákladové ceny, protože transakci nebylo možné úplně vyrovnat. Předtím, než je tato zpráva zobrazena, systém hlásí číslo zboží a příslušné transakce. Tato zpráva informuje o tom, že částka nákladů použitá pro tuto transakci nebyla jako důsledek uzávěrky skladu aktualizována. Tato zpráva se zobrazí, pokud transakce typu „výdej“ nelze vyrovnat. Během procesu uzávěrky skladu systém provede kontrolu pro každou finanční dimenzi, aby se zjistilo, zda do specifikovaného data uzávěrky existuje více výdejů než příjmů. Tento typ nevyrovnanosti může nastat tehdy, když skladová transakce z nákupní objednávky není plně zaúčtována finančně, protože faktura dodavatele ještě nebyla dodána, nebo protože položka kusovníku zahrnutá do výroby na vyšší úrovni není finančně zaúčtována. (Odvozenou výrobu není vypočtené náklady.) V takovém případě následné uzavření neupraví všechny výdeje na správné nákladové ceny, protože nedostatek příjmu informací je k dispozici. Před každým spuštěním uzávěrky systém určí, zda protokol, který obsahuje upozornění, je uložen a lze jej zobrazit. Pokud jste zdrojem velkého počtu varování, je doporučeno provést následující akce:

-   Finanční aktualizace příjmů.
-   Posuňte datum uzávěrky.
-   Přehodnoťte své obchodní postupy.

V některých případech nemusí být možné provádět žádné akce pro uvedená upozornění. Když se například označení použije u označené nákupní objednávky, která má finanční datum po datu uzávěrky, nelze datum uzávěrky změnit.

## <a name="reversing-a-completed-inventory-close"></a>Zrušení dokončené uzávěrky skladu
V některých případech je nutné zrušit dokončenou uzávěrku skladu a vrátit vyrovnání do původního stavu před provedením úprav. Při zrušení dokončené uzávěrky skladu budou zásoby také znovu otevřeny, aby bylo možné účtovat do příslušného období, které pokrývá uzávěrku skladu. Související změny také mohou být udělány v hlavní knize. Po dokončení množství úprav můžete spustit znovu uzávěrku skladu pro období, ve kterém pracujete. **Poznámka:** Znovu otevřít lze pouze poslední zásoby období, které bylo ukončeno. Pokud chcete stornovat předchozí skladové uzávěrky, je nutné stornovat postupně každou následnou skladovou uzávěrku, počínaje poslední uzávěrkou.


