---
title: Pole hmotnosti na řádcích nákladu neodpovídají polím hmotnosti na nákladu
description: Pole hmotnosti na řádcích nákladu neodpovídají polím hmotnosti na nákladu
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSShipmentDetails_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f71ac7b2777cb77fccdf1a4c72a47c9b406bbd68b2d20c41ddc96028d2ffc348
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756696"
---
# <a name="the-weight-fields-on-load-lines-dont-match-the-weight-fields-on-the-load"></a>Pole hmotnosti na řádcích nákladu neodpovídají polím hmotnosti na nákladu

Kódy chyb: WHSLoadWeightOnLinesDoNotMatchLoadWarning

## <a name="symptoms"></a>Příznaky

Systém zobrazuje následující chybovou zprávu:

> Pole hmotnosti na řádcích nákladu neodpovídají polím hmotnosti na nákladu %1. Spusťte kontrolu konzistence hmotnosti nákladu skladu a přepočítejte pole hmotnosti.

## <a name="cause"></a>Příčina

Pole **Čistá hmotnost** a **Hmotnost obalu** jsou nastavena na řádku nákladu na hodnotu *0* (nula). Pole hmotnosti však nejsou nastavena na hodnotu *0* pro měření hmotnosti na produktu. Pokud pole hmotnosti nejsou nastavena na řádku nákladu, jakékoli opravy množství na řádku nákladu mohou způsobit nesprávný výpočet hmotnosti na nákladu. K tomuto problému může dojít, pokud se od vytvoření řádku nákladu změnily hmotnosti na produktu.

## <a name="resolution"></a>Rozlišení

Ve výchozím nastavení se při vytváření řádku nákladu zadávají pole hmotnosti z produktu. Pokud je hmotnost nulová, můžete ji přepočítat pomocí funkce *Kontrola konzistence hmotnosti nákladu skladu*.

1. Přejděte k nabídce **Správa systému \> Periodické úkoly \> Databáze \> Kontrola konzistence**.
1. V dialogovém okně **Kontrola konzistence** nastavte pole **Modul** na hodnotu *Řízení skladu*.
1. Nastavte pole **Kontrola / oprava** na hodnotu *Opravit chybu*.
1. V seznamu zaškrtávacích políček vyberte zaškrtávací políčko **Kontrola konzistence hmotnosti nákladu skladu** a ujistěte se, že je zvýrazněn pouze řádek pro toto zaškrtávací políčko.
1. V horní části seznamu zaškrtávacích políček vyberte tlačítko se třemi tečkami (**...**) a poté v nabídce vyberte možnost **Dialogové okno**.
1. V dialogovém okně **Kontrola konzistence hmotnosti nákladu skladu** nastavte následující pole a určete kritéria, podle kterých by měla probíhat kontrola konzistence:

    - **ID nákladu:** Zadejte ID nákladu. Chcete-li zkontrolovat všechna ID nákladu, ponechte toto pole prázdné.
    - **Číslo položky:** Zadejte číslo položky. Chcete-li zkontrolovat všechny položky, ponechte toto pole prázdné.
    - **Vždy přepočítávat hmotnost nákladů:** Tuto možnost nastavte na hodnotu *Ano*.
    - **Povolit přepsání hmotnosti na řádcích nákladu:** Tuto možnost nastavte na hodnotu *Ano*.

1. Výběrem tlačítka **OK** zavřete dialogové okno **Kontrola konzistence hmotnosti nákladu skladu**.
1. Vyberte tlačítko se třemi tečkami a poté v nabídce vyberte možnost **Spustit**.

Hmotnost se přepočítá na základě zadaných kritérií. Vyberte odkaz **Podrobnosti zprávy** k zobrazení výsledku kontroly konzistence.
