<span class="tooltip-source">
    <slot name="content" />
    <span class="tooltip">
        <slot name="description" />
    </span>
</span>

<style>
    span.tooltip-source {
        font-size: 80%;
        margin-left: 5px;
        position: relative;
    }

    span.tooltip {
        opacity: 0;
        transition: opacity 0.6s;

        position: absolute;
        left: 50%;
        bottom: 100%;
        transform: translate(var(--transformx, -50%), var(--transformy, -5px));
        width: var(--width);

        color: #000;
        background-color: #fff;
        line-height: 1.2;
        text-align: center;
        pointer-events: none;
        border-radius: 5px;
        padding: 1px 3px;
        box-shadow: 0 0 3px #999;
    }

    span.tooltip-source:hover span.tooltip {
        opacity: 1;
    }
</style>
