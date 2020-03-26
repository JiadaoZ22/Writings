# LaTeX-Guide

## Math

### Alignment

> https://www.overleaf.com/learn/latex/aligning_equations_with_amsmath
>
> ```latex
> \begin{aligned} 
> 2x - 5y &=  8 \\ 
> 3x + 9y &=  -12
> \end{aligned}
> ```
>
> 

## Grammar

### Font Style

> **typewriter font**
>
> ```
> \texttt{balabala}
> ```
>
> ![image-20200325180710573](LaTeX-Guide.assets/image-20200325180710573.png)

### Reference

> **Design the style**
>
> ```latex
> \usepackage{xcolor}
> \hypersetup{
>   colorlinks   = true, %Colours links instead of ugly boxes
>   urlcolor     = blue, %Colour for external hyperlinks
>   linkcolor    = blue, %Colour of internal links
>   citecolor   = red %Colour of citations
> }
> ```

### Table

> ```latex
> \begin{table}
> \caption{Confusion matrix for classification of continuous hand gestures on the Moto dataset
> }
> \centering
> \begin{tabular}{cccccccc}
> 
> \hline
>    & \textbf{Left} & \textbf{Right}  & \textbf{Up} & \textbf{Down} & \textbf{Back\&Forth} & \textbf{Clockwise} & \textbf{Counterclockwise} \\
>   \hline
>   \textbf{Left}  & 28 & 0 & 0  & 0 & 0 & 0 & 6\\
> 
>   \textbf{Right}  & 0 & 40 & 0  & 0 & 0 & 0 & 0\\
> 
>   \textbf{Up}  & 0 & 0 & 36  & 0 & 2 & 0 & 0\\
> 
>   \textbf{Down} & 0 & 0 & 0  & 29 & 0 & 0 & 0\\
> 
>   \textbf{Back\&Forth}  & 0 & 0 & 0  & 0 & 44 & 0 & 0\\
> 
>   \textbf{Clockwise}  & 2 & 0 & 0  & 0 & 0 & 23 & 0\\
> 
>   \textbf{Counterclockwise}  & 0 & 0 & 0  & 0 & 0 & 0 & 23\\
>   \hline
>   
> \end{tabular}
> \label{table:Recog Accuracy in continuous gesture}
> \end{table}
> ```
>
> ![image-20200325173447140](LaTeX-Guide.assets/image-20200325173447140.png)

### Figure

> ```latex
> \begin{figure}
>     \centering
>     \begin{minipage}{0.48\textwidth}
>         \includegraphics[width=0.95\linewidth]{figures/ContinuousSegmentAccuracy}
>         \caption{Segmentation and recognition accuracy of the continuous hand gesture recognition algorithm on the Moto dataset. Sub1 means human subject one}
>         \label{fig:ContinuousSegmentAccuracy}
>     \end{minipage}
>     \begin{minipage}{0.48\textwidth}
>         \includegraphics[width=0.9\linewidth]{figures/ContinuousSegmentAccuracy_UG}
>         \caption{Segmentation and recognition accuracy of the continuous hand gesture recognition algorithm on the UG dataset. Sub1 means human subject one}
>         \label{fig:ContinuousSegmentAccuracy_UG}
>     \end{minipage}
> \end{figure}
> ```
>
> ![image-20200325173705876](LaTeX-Guide.assets/image-20200325173705876.png)



> ```latex
> \begin{wrapfigure}{R}{3in}
> \centering
> \includegraphics[width=2.97in]{figures/SegmentAccuracy_Window}
> \caption{Precision, recall and accuracy under different window size}
> \label{fig:window}
> \end{wrapfigure}
> ```
>
> ![image-20200325175924975](LaTeX-Guide.assets/image-20200325175924975.png)

