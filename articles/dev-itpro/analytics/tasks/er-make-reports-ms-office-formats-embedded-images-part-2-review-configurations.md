--- 
title: "Kontrola konfigurací pro provedení sestav ve formátu Microsoft Office s integrovanými obrázky pro elektronické výkaznictví (ER)"
description: "K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky průvodce záznamem úloh Vytváření sestav ER ve formátu MS Office s vloženými obrázky (část 1 - nastavení parametrů)."
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: dcc162a4c0ba81079eefb7564ab037c1287acd92
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="review-configurations-to-make-reports-in-microsoft-office-formats-with-embedded-images-for-electronic-reporting-er"></a>Kontrola konfigurací pro provedení sestav ve formátu Microsoft Office s integrovanými obrázky pro elektronické výkaznictví (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky průvodce záznamem úloh Vytváření sestav ER ve formátu MS Office s vloženými obrázky (část 1: nastavení parametrů).

Tento postup popisuje proces navrhování konfigurací elektronického vykazování (ER) pro generování elektronických dokumentů obsahujících vložené obrázky v aplikaci Microsoft Excel a Microsoft Word. V tomto příkladu si prohlédnete konfigurace ER pro vzorovou společnost Litware, Inc. 

Tento postup je navržen pro uživatele s přiřazenou rolí správce systému nebo vývojáře elektronického vykazování. Kroky lze dokončit za použití datové sady USMF.


## <a name="review-the-imported-data-model"></a>Kontrola importovaného datového modelu
1. Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.
2. Ve stromové struktuře zvolte Model pro šeky.
3. Klikněte na možnost Návrhář.
    * Tento model je určen pro reprezentaci platebních šeků z obchodního hlediska a mapování tohoto modelu ke zdrojům dat aplikace. Zkontrolujte tento model návrhářem operací ER. Povšimněte si atributů prvků modelu, které jsou uvedeny: struktura, název, popis, datový typ a tak dále.   
4. Ve stromovém zobrazení rozbalte Kořen.
5. Ve stromovém zobrazení vyberte root\cheques.
6. Ve stromovém zobrazení rozbalte root\cheques.
7. Ve stromovém zobrazení rozbalte root\cheques\attributes.
8. Ve stromovém zobrazení rozbalte root\payer.
9. Ve stromovém zobrazení vyberte root\istestrun.
10. Ve stromovém zobrazení vyberte root\layout.
    * Prvek rozvržení tohoto modelu představuje podrobné informace o tisku rozvržení formuláře šeku pro vybraný bankovní účet. Dále zahrnuje dva uzly pro Typ datového kontejneru k ukládání obrázků.   
11. Ve stromovém zobrazení rozbalte root\layout.
12. Ve stromovém zobrazení vyberte root\layout\company log.
13. Ve stromovém zobrazení rozbalte root\layout\company logo.
14. Ve stromovém zobrazení vyberte root\layout\company logo\image.
15. Ve stromovém zobrazení vyberte root\layout\company logo\isprinted.
16. Ve stromovém zobrazení vyberte root\layout\signature.
17. Ve stromovém zobrazení rozbalte root\layout\signature.
18. Ve stromovém zobrazení vyberte root\layout\signature\image.
19. Ve stromovém zobrazení vyberte root\layout\signature\isprinted.
    * Všimněte si, že dva elementy modelu dat obrázku jsou vázány k polím tabulky s obrázky loga společnosti a podpisu oprávněné osoby v binárním formátu.  
20. Ve stromovém zobrazení rozbalte root\layout\watermark.
21. Klikněte na možnost Mapovat model na datový zdroj.
22. Klikněte na možnost Návrhář.
23. Ve stromovém zobrazení rozbalte chequesselected.
24. Ve stromové struktuře rozbalte Rozvržení.
25. Ve stromovém zobrazení rozbalte layout\company logo.
26. Ve stromovém zobrazení rozbalte layout\signature.
27. Ve stromovém zobrazení rozbalte layout\watermark.
28. Přepnutím aktivujte 'Zobrazit podrobnosti'.
    * Všimněte si, že prvek datového modelu šeků má vazbu na tabulku TmpChequePrintout, která za běhu bude obsahovat záznamy šeků, které uživatel vybral pro tisk.   
29. Zavřete stránku.
30. Zavřete stránku.
31. Zavřete stránku.

## <a name="review-the-imported-format"></a>Kontrola importovaného formátu
1. Ve stromové struktuře rozbalte Model pro šeky.
2. Ve stromovém zobrazení vyberte Model for cheques\Cheques printing format.
3. Klikněte na možnost Návrhář.
4. Klikněte na Přílohy.
5. Klikněte na možnost Otevřít.
    * Otevřete připojenou šablonu sestavy v aplikaci Excel.  
    * Zkontrolujte šablonu Excel připojené sestavy, která bude použita pro tisk šeků. Šablona obsahuje dva šeky na každé stránce a je určena pro tisk šeků na předtištěném formuláři. Všimněte si, že jsou vloženy dva prázdné obrázky. Tyto prázdné obrázky jsou logo společnosti a podpis osoby, která autorizovala platbu. Ověřte, že jsou obrázky pojmenovány v aplikaci Excel jako CompLogo a SignatureImage.   
6. Zavřete stránku.
7. Ve stromovém zobrazení rozbalte Sestava.
8. Ve stromovém zobrazení rozbalte Report\ChequeLines.
9. Ve stromovém zobrazení vyberte Report\ChequeLines\CompLogo.
10. Přepnutím aktivujte 'Zobrazit podrobnosti'.
    * Všimněte si, že prvek buňky ve formátu CompLogo představuje položku Excel, která slouží k načtení obrázku loga společnosti v sestavě. Tento prvek formátu má vazbu na element datového modelu obrázku, který za běhu obsahuje obrázek loga společnosti v binárním formátu.   
11. Klikněte na kartu Mapování.
12. Klikněte na Úprava povolena.
    * Poznámka: můžete nastavit element buňky ve formátu "CompLogo" tak, aby již nebyl povolen. V takovém případě se na přidruženém prvku obrázku Excel skryje logo společnosti ve vygenerované sestavě. Pokud se u povoleného výrazu vrátí hodnota TRUE, a definovaná vazba nepřinese žádný obrázek, přidružený prvek obrázku Excel bude obsahovat obrázek, který byl uložen v šabloně aplikace Excel.   
13. Zavřete stránku.
14. Ve stromovém zobrazení rozbalte Štítky: Kontejner.
    * Některé popisky, které jsou uvedeny v předtištěném formuláři šeků, budou zahrnuty do sestavy při jejím vytvoření pro účely testování. Tyto štítky se však nevytisknou během skutečného tisku, protože předtištěný formulář je již obsahuje.  
15. Zavřete stránku.


