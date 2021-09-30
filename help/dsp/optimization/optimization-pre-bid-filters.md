---
title: Vorab-Angebotsfilter auf Platzierungsebene und deren Verwendung
description: Verweisen Sie auf die verfügbaren Filter auf Platzierungsebene vor dem Angebot und sehen Sie, wie sie verwendet werden.
feature: DSP Optimization
exl-id: c699e970-84ca-429b-8062-81804e6c9f21
source-git-commit: 75ec6f54271542d56e0d16fbb7aa92ebcf00d765
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# Vorab-Angebotsfilter auf Platzierungsebene und deren Verwendung

| Vorab-Angebotsfilter | Beschreibung | Verwendung dieses Filters |
| ---------------| ----------- | ---------------------- |
| [!UICONTROL Click Through Rate] | Legt einen Mindestschwellenwert für die Vorhersage der Wahrscheinlichkeit fest, mit der eine Auktion zu einem Clickthrough führt. Wenn Sie beispielsweise den Schwellenwert auf 0,1 % setzen, bieten Sie kein Angebot für eine Auktion an, es sei denn, die prognostizierte Wahrscheinlichkeit eines Klicks ist größer oder gleich 0,1 %.<br><br><b>Hinweis:</b> Filter werden vor Optimierungszielen angewendet. Daher können sehr strenge Filter Ausgaben verhindern. | Verwenden Sie diese Option, wenn Sie ein KPI-Mindestziel für die Clickthrough-Rate (CTR) haben und Ihr Budget nicht ausgeben möchten, wenn die CTR unter dem Schwellenwert liegt. Dieser Filter kann sehr restriktiv sein, daher ist es wichtig, realistische Ziele festzulegen. Je nach anderen Einschränkungen der Platzierung ist ein Ziel von 0,03-0,07 % im Allgemeinen ein guter Ausgangspunkt. Sie können dies bei Bedarf auf Site-Ebene optimieren, um die Metriken zu verbessern.<br><br>Wenn Sie eine minimale CTR und den bestmöglichen CPM erreichen möchten, wird empfohlen, einen  [!UICONTROL Click Through Rate] Filter mit dem Optimierungsziel &quot;[!UICONTROL Lowest CPM]&quot;zu kombinieren. Wenn Ihr Ziel ein maximaler CPM ohne echten Nutzen für eine Übererfüllung und eine minimale CTR ist, kann es angemessener sein, einen [!UICONTROL Click Through Rate]-Filter mit dem Optimierungsziel &quot;[!UICONTROL Always Max Bid + Highest CTR]&quot;zu koppeln. |
| [!UICONTROL 100% Completion Rate] | Legt eine erforderliche minimale Abschlussrate fest, die erfüllt sein muss, bevor Sie ein Angebot für eine Impression abgeben. | Verwenden Sie diesen Filter, wenn das Hauptziel der Kampagne die Abschlussraten sind. Faktor in anderen Targeting-Parametern, aber 65% ist der empfohlene Anfangsprozentsatz. |
| [!UICONTROL Player Size - Adobe] | Legt mithilfe von Daten aus Advertising Cloud DSP eine erforderliche minimale Player-Größe fest. Sie werden ein Gebot für eine Impression abgeben, wenn der Schwellenwert [!UICONTROL Player Size] erreicht ist. | Verwenden Sie , um sicherzustellen, dass Sie mit Daten aus DSP ein Inventar für den vollständigen Episode-Player bereitstellen. |
| [!UICONTROL Player Size 3rdParty (Moat/IAS)] | Legt eine erforderliche minimale Player-Größe mithilfe von Daten von [!DNL Moat] oder [!DNL Integral Ad Science] ([!DNL IAS]) fest. Sie werden ein Gebot für eine Impression abgeben, wenn der Schwellenwert [!UICONTROL Player Size] erreicht ist. | Verwenden Sie , um sicherzustellen, dass Sie mit plattformweiten [!DNL Moat]- oder [!DNL IAS]-Daten ein Inventar für den Full-Episode-Player bereitstellen.<br><br><b>Hinweis:</b> Verwenden Sie diesen Filter nur, wenn die Kampagne für die Verwendung von  [!DNL Moat] oder - [!DNL IAS] Daten konfiguriert ist. |
| [!UICONTROL Viewability Adobe (MRC or [!DNL GroupM])] | Legt einen erforderlichen Mindestprozentsatz für die Sichtbarkeit fest, wobei Advertising Cloud DSP-Darstellungszahlen und -Messungen verwendet werden. Sie bieten eine Impression an, wenn der angegebene Schwellenwert erreicht ist.<br><br><b>Hinweise:</b><ul><li>Wenn die Einstellung [!UICONTROL Viewability Sensitivity] der Kampagne &quot;[!UICONTROL Standard (50% of ad in view for 2 consecutive seconds)]&quot;lautet, wird der Standard für die Sichtbarkeitsmessung (MRC) für die Kampagne verwendet. [!DNL Media Rating Council] Wenn die [!UICONTROL Viewability Sensitivity]-Einstellung &quot;[!UICONTROL Strict (100% of ad in view & audio on for 50% duration)]&quot;ist, wird für die Kampagne der Standard für die Sichtbarkeitsmessung verwendet.[!DNL GroupM]</li><li>Adobe-Messdefinitionen unterscheiden sich von Drittanbieterdefinitionen, sodass es geringfügige Diskrepanzen mit Drittanbieterdaten geben kann.</li></ul> | Die Best Practice besteht darin, das Optimierungsziel und alle Filtereinstellungen vor dem Angebot mit der Einstellung [!UICONTROL Viewability Sensitivity] der Kampagne abzustimmen. |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [Wie DSP Ihre Kampagnen optimiert](optimization-how-dsp-optimizes-campaigns.md)
>* [Paketeinstellungen](/help/dsp/campaign-management/packages/package-settings.md)
>* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Kampagneneinstellungen](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [Optimierungsziele und Verwendung](optimization-goals.md)

