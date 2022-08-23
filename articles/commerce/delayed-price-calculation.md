---
title: Odložení přesné kalkulace ceny a slevy kvůli vyššímu výkonu
description: Tento článek popisuje schopnost zpožděného výpočtu ceny, která je k dispozici v pokladním místě Microsoft Dynamics 365 Commerce (POS) a kontaktním středisku.
author: boycezhu
ms.date: 09/09/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: boycez
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 66c7c5a61648ba0423b27b74a1c4e42bc1b22b8b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267583"
---
# <a name="delay-exact-price-and-discount-calculation-for-improved-performance"></a>Odložení přesné kalkulace ceny a slevy kvůli vyššímu výkonu

[!include [banner](includes/banner.md)]

Tento článek popisuje schopnost zpožděného výpočtu ceny, která je k dispozici v pokladním místě Microsoft Dynamics 365 Commerce (POS) a kontaktním středisku.

Dynamics 365 Commerce podporuje vytváření víceřádkových slev, které se použijí při kombinaci více prodejních řádků prodejní objednávky nebo prodejní nabídky. Tyto slevy zahrnují kombinační, mezní a množstevní slevy.

Kdykoli je do objednávky přidán nový řádek, cenový modul Commerce vyhodnotí celý košík a určí, zda lze použít některou z těchto víceřádkových slev. Kvůli tomuto přepočtu může přidání nových řádků ovlivnit výkon při zvětšování prodejní objednávky.

Společnosti obchodující v režimu B2B a některé společnosti obchodující v režimu B2C však často mají velké objednávky. Proto může dokončení přepočtu, který nástroj pro tvorbu cen provádí po přidání každé položky do košíku, trvat delší dobu. Navíc u velkých objednávek obvykle není příliš důležité, aby se ihned po každém vložení položky do košíku zobrazila přesná cena a sleva. Mnohem důležitější je to, aby uživatelé mohli rychle přidávat položky. Schopnost oddálit přesnou kalkulaci ceny a slevy, dokud o to uživatel nepožádá nebo není dokončena objednávka, může výrazně zlepšit výkon. Může to také zkrátit čas potřebný k dokončení objednávky.

Možnost odložení přesného výpočtu ceny a slevy je v POS již dlouho k dispozici. Od vydání Commerce 10.0.22 je k dispozici také pro kontaktní středisko.

## <a name="enable-delayed-price-and-discount-calculation-for-pos"></a>Povolení odloženého výpočtu ceny a slevy pro POS

Chcete-li povolit odložení výpočtu ceny a slevy pro POS,, postupujte takto.

1. V Commerce Headquarters přejděte na profil funkcí, který je přidružen k fyzickému úložišti.
1. Na záložce **Množství** povolte konfiguraci **Ručně vypočítat slevy několika položek**.
1. Otevřete návrháře rozložení obrazovky pro registry, kde by měl být povolen zpožděný výpočet.
1. Přidejte tlačítko pro operaci **Vypočítat součet** na požadovanou mřížku tlačítek.
1. Spusťte úlohy **1070** a **1090**.

Nyní, když jsou položky přidány k transakci, víceřádkové slevy se spočítají až poté, kdy pokladník vybere tlačítko **Vypočítat součet**. Po výběru tlačítka **Vypočítat součet** pro transakci se pro ni vždy vypočítají víceřádkové slevy. Pokladník nebude muset znovu vybírat tlačítko, i když jsou do košíku přidány další položky. Systém nedovolí pokladníkovi zachytit platbu, dokud nebude vybráno tlačítko **Vypočítat součet**.

## <a name="enable-delayed-price-and-discount-calculation-for-call-center"></a>Povolení odloženého výpočtu ceny a slevy pro kontaktní středisko

Chcete-li povolit odložení výpočtu ceny a slevy pro kontaktní středisko, postupujte takto.

1. V Commerce Headquarters přejděte do nabídky **Pracovní prostory \> Správa funkcí**.
1. Povolte funkci **Zabraňte neúmyslnému výpočtu ceny pro obchodní objednávku**. Tato funkce je předpokladem pro funkci zpožděného výpočtu ceny a slevy.

    > [!NOTE]
    > U nových nasazení je funkce **Zabraňte neúmyslnému výpočtu ceny pro obchodní objednávku** ve výchozím nastavení povolena.

1. Přejděte do nabídky **Parametry obchodu \> Ceny a slevy**.
1. V části **Různé** povolte konfiguraci **Ručně vypočítat víceřádkové ceny a slevy**.

Nyní, když je v kontaktním středisku vytvořena nebo upravena prodejní objednávka nebo prodejní nabídka, přesná kalkulace ceny a slevy pro ni bude opožděna. Nástroj pro určování cen bude brát do úvahy pouze prodejní řádek, který se přidává nebo upravuje, a bude ignorovat všechny ostatní prodejní řádky. Čistá částka za položku zahrnuje výpočet ceny a jednoduché slevy (procento slevy nebo sleva na jednotlivou položku). Slevy kombinační, mezní a množstevní však nebudou uplatněny. Uživatelé kontaktního střediska, kteří si chtějí zobrazit přesnou cenu včetně všech slev, mohou vybrat jedno ze tří tlačítek: **Přepočítat**, **Celkem**, nebo **Dokončit**.

> [!NOTE]
> U objednávek kontaktního střediska systém zobrazí varovnou zprávu, která uživateli připomene, že pro přesnou kalkulaci ceny a slevy, která má být provedena, si musí vybrat tlačítko **Přepočítat**, **Celkem** nebo **Dokončit**. U objednávek, kde je k dispozici tlačítko **Dokončit**, neexistuje žádný způsob, jak by uživatel kontaktního střediska mohl vynechat kalkulaci přesné ceny a slevy, protože k dokončení zachycení objednávky musí vybrat tlačítko **Dokončit**. U objednávek, kde tlačítko **Dokončit** není k dispozici, se neprovádí žádná akce, která by indikovala dokončení zachycení objednávky. Proto je tedy uživatel kontaktního střediska zodpovědný za výběr jedné z možností **Přepočítat** nebo **Celkem** před dokončením zachycení objednávky.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
